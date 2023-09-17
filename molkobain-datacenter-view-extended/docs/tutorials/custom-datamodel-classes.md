<button onclick="history.back()">Back</button>

# Custom datamodel classes

* [Introduction](#introduction)
* [Step 1 - Class requirements](#step-1---class-requirements)
* [Step 2 - Class registration](#step-2---class-registration)
* [Frequent questions](#frequent-questions)
  * [Where can I find an example for a custom class?](#where-can-i-find-an-example-for-a-custom-class)

## Introduction

Out of the box, only certain classes of objects can be displayed in the graphical view of racks and enclosure:

* For a `Rack`, classes deriving from either `Enclosure` or `DatacenterDevice`.
* For an `Enclosure`, only classes deriving from `DatacenterDevice`.

If you customized the datamodel and added your own classes, you might want to display them in the graphical view even though they don't have the previously mentioned classes as parent.

## Step 1 - Class requirements

The classes MUST match some requirements in order to be used in the graphical view. If one of the requirements if not fullfilled, class will not be displayed or may crash the app.

Have the following attributes:

| Code                 | Label                | Type                 | Description                                                                                                                                              |
|----------------------|----------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| rack_id              | Rack                 | AttributeExternalKey | External key to the `Rack` class                                                                                                                         |
| enclosure_id         | Enclosure            | AttributeExternalKey | External key to the `Enclosure` class                                                                                                                    |
| position_p           | Panel                | AttributeEnum        | `Enclosure` panel (or `Rack` panel if directly in it) the element is for, values can be `"front"` or `"rear"`                                            |
| position_v           | Vert. position       | AttributeMHFRackUnit | Vertical position (U) of the element in the `Enclosure` (or `Rack` if mounted directly on int). (Must be the bottom position, not top)                   |
| position_h           | Hori. position       | AttributeInteger     | Horizontal position of the element in its `Enclosure` (Must be the left side, not right). This ONLY applies if its `Enclosure`'s layout is set to 'Grid' |
| nb_u                 | Height               | AttributeMHFRackUnit | Height in units (U)                                                                                                                                      |
| nb_cols              | Width                | AttributeInteger     | Width of the slot defined by on how many grid columns it spreads. This ONLY applies if its `Enclosure`'s layout is set to 'Grid'                         |
| zero_u               | Zero-U               | AttributeEnum        | Only set to 'Yes' for devices that do not fit in standard racks / enclosures layout (eg. vertical PDU)                                                   |
| weight               | Weight               | AttributeDecimal     | Weight of the device itself                                                                                                                              |
| expected_power_input | Expected power input | AttributeInteger     | Expected power consumption of the device                                                                                                                 |

Have the following methods:

| Name            | Visibility | Static | Arguments | Return type | Description                                                                                                         |
|-----------------|------------|--------|-----------|-------------|---------------------------------------------------------------------------------------------------------------------|
| GetEndPositionV | public     | No     | None      | `integer`   | Return on which U is positioned the top side of the device                                                          |
| GetEndPositionH | public     | No     | None      | `integer`   | Return on which column of the grid is positioned the right side of the device (used only for grid layout enclosure) |
| IsMounted       | public     | No     | None      | `bool`      | Return if the device is mounted in an host (rack / enclosure)                                                       |

_Note: You'll find a class example in the frequent questions at the end of this page to bootstrap you._

## Step 2 - Class registration

Once your classes have the requirements, you need to register them so they will be used in the graphical view. To do so, just add them in the configuration file for the `custom_device_classes` parameter. \
For example if you have 2 classes named "CustomClassA" and "CustomClassB":

```php
'molkobain-datacenter-view-extended' => array (
    'custom_device_classes' => ['CustomClassA', 'CustomClassB'],
),
```

And that's it!

## Frequent questions

### Where can I find an example for a custom class?

Here is an example of a custom class with all necessary attributes and methods. Of course mind to change its name, DB table and adjust it to your class' specifities.

```xml
<?xml version="1.0" encoding="UTF-8"?>
<itop_design xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" version="1.6">
  <classes>
    <class id="CustomClassA" _delta="define">
      <properties>
        <category>bizmodel,searchable</category>
        <abstract>false</abstract>
        <db_table>customclassa</db_table>
      </properties>
      <fields>
        <field id="name" xsi:type="AttributeString">
          <sql>name</sql>
          <default_value/>
          <is_null_allowed>true</is_null_allowed>
          <validation_pattern/>
          <tracking_level>all</tracking_level>
        </field>
        <field id="nb_u" xsi:type="AttributeString">
          <sql>nb_u</sql>
          <default_value/>
          <is_null_allowed>true</is_null_allowed>
          <validation_pattern/>
          <tracking_level>all</tracking_level>
        </field>
        <field id="nb_cols" xsi:type="AttributeInteger">
          <sql>nb_cols</sql>
          <default_value>1</default_value>
          <is_null_allowed>false</is_null_allowed>
        </field>
        <field id="position_p" xsi:type="AttributeEnum">
          <sql>position_p</sql>
          <values>
            <value id="front">front</value>
            <value id="rear">rear</value>
          </values>
          <default_value>front</default_value>
          <is_null_allowed>false</is_null_allowed>
          <display_style>list</display_style>
        </field>
        <field id="position_v" xsi:type="AttributeInteger">
          <sql>position_v</sql>
          <default_value/>
          <is_null_allowed>true</is_null_allowed>
          <tracking_level>all</tracking_level>
        </field>
        <field id="position_h" xsi:type="AttributeInteger">
          <sql>position_h</sql>
          <default_value/>
          <is_null_allowed>true</is_null_allowed>
        </field>
        <field id="rack_id" xsi:type="AttributeExternalKey">
          <sql>rack_id</sql>
          <filter/>
          <dependencies/>
          <is_null_allowed>true</is_null_allowed>
          <target_class>Rack</target_class>
          <on_target_delete>DEL_AUTO</on_target_delete>
          <tracking_level/>
        </field>
        <field id="enclosure_id" xsi:type="AttributeExternalKey">
          <sql>enclosure_id</sql>
          <filter/>
          <dependencies>
            <attribute id="rack_id"/>
          </dependencies>
          <is_null_allowed>true</is_null_allowed>
          <target_class>Enclosure</target_class>
          <on_target_delete>DEL_AUTO</on_target_delete>
          <tracking_level/>
        </field>
        <field id="zero_u" xsi:type="AttributeEnum">
            <values>
                <value id="yes">yes</value>
                <value id="no">no</value>
            </values>
            <sql>zero_u</sql>
            <default_value>no</default_value>
            <is_null_allowed>false</is_null_allowed>
            <display_style>list</display_style>
        </field>
        <field id="weight" xsi:type="AttributeDecimal">
            <sql>weight</sql>
            <default_value/>
            <is_null_allowed>true</is_null_allowed>
            <digits>8</digits>
            <decimals>3</decimals>
        </field>
        <field id="expected_power_input" xsi:type="AttributeInteger">
            <sql>expected_power_input</sql>
            <default_value/>
            <is_null_allowed>true</is_null_allowed>
        </field>
      </fields>
      <methods>
        <method id="GetEndPositionV">
          <comment><![CDATA[/**
	 * Returns object ending U (eg. A 4U object positioned at 10U will return 13)
	 *
	 * @return int
	 */]]></comment>
          <static>false</static>
          <access>public</access>
          <type>Overload-DBObject</type>
          <code><![CDATA[	public function GetEndPositionV()
	{
		$iHeight = ((int) $this->Get('nb_u') > 0) ? $this->Get('nb_u') : 1;
		$iPositionV = (int) $this->Get('position_v');

		return $iPositionV + $iHeight - 1;
	}]]></code>
        </method>
        <method id="GetEndPositionH">
          <comment><![CDATA[/**
	 * Returns object ending col. (eg. A 4 cols. object positioned at col. 2 will return 5)
	 *
	 * @return int
	 */]]></comment>
          <static>false</static>
          <access>public</access>
          <type>Overload-DBObject</type>
          <code><![CDATA[	public function GetEndPositionH()
	{
		$iWidth = ((int) $this->Get('nb_cols') > 0) ? $this->Get('nb_cols') : 1;
		$iPositionH = (int) $this->Get('position_h');

		return $iPositionH + $iWidth - 1;
	}]]></code>
        </method>
        <method id="IsMounted">
          <comment><![CDATA[/**
	 * Returns true if object is mounted in its host (position_v > 0)
	 *
	 * @return bool
	 */]]></comment>
          <static>false</static>
          <access>public</access>
          <type>Overload-DBObject</type>
          <code><![CDATA[	public function IsMounted()
	{
		$iPositionV = (int) $this->Get('position_v');

		return $iPositionV > 0;
	}]]></code>
        </method>
      </methods>
      <presentation>
        <list>
          <items/>
        </list>
        <search>
          <items/>
        </search>
        <details>
          <items>
            <item id="col:col0">
              <items>
                <item id="name">
                  <rank>10</rank>
                </item>
                <item id="rack_id">
                  <rank>20</rank>
                </item>
                <item id="enclosure_id">
                  <rank>30</rank>
                </item>
                <item id="position_p">
                  <rank>40</rank>
                </item>
                <item id="position_v">
                  <rank>50</rank>
                </item>
                <item id="position_h">
                  <rank>60</rank>
                </item>
                <item id="nb_u">
                  <rank>70</rank>
                </item>
                <item id="nb_cols">
                  <rank>80</rank>
                </item>
              </items>
              <rank>10</rank>
            </item>
          </items>
        </details>
      </presentation>
      <parent>cmdbAbstractObject</parent>
    </class>
  </classes>
</itop_design>
```