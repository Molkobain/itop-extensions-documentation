# Configuration parameters

Some parameters are inherited from the simple version of the extension, others are from the extended version, but all are detailled below. \
Either way, they should already be present in your configuration file to ease the configuration.

## Parameters of the simple version
  * `enabled` Enable / disable the graphical part of the extension without having to uninstall it (datamodel changes will remain). Value can be `true` or `false`.
  * `device_tooltip_attributes` Specify which attributes to display in the device [tooltip](../features/graphical-tab-overview.md) on hover. Must be an array of object classes pointing to an array of attributes (see example below).

*Default values:*
```
'molkobain-datacenter-view' => array(
    'enabled' => true,
    'device_tooltip_attributes' => array(
        'DatacenterDevice' => array(
            'brand_id',
            'model_id',
            'serialnumber',
            'asset_number',
        ),
        'NetworkDevice' => array(
            'networkdevicetype_id',
            'brand_id',
            'model_id',
            'ram',
            'serialnumber',
            'asset_number',
        ),
        'Server' => array(
            'brand_id',
            'model_id',
            'osfamily_id',
            'cpu',
            'ram',
            'serialnumber',
            'asset_number',
        ),
    ),
),
```

## Parameters of the extended version
  * `enabled` Enable / disable the graphical part of the extension without having to uninstall it (datamodel changes will remain). Value can be `true` or `false`.
  * `debug` Enable / disable debug information the JS console, enable it only when troubleshooting. Value can be `true` or `false`.
  * `display_consistency_checks` Display or not the [consistency checks](../features/consistency-checks.md) when updating / viewing an element. Value can be `true` or `false`.
  * `enforce_consistency_checks` Whether the [consistency checks](../features/consistency-checks.md) are blocking when when updating / creating an element. Value can be `true` or `false`.
  * `custom_device_classes` List of [custom datamodel classes](docs/tutorials/custom-datamodel-classes.md) to display in the graphical view even though they don't derive from the excepted datamodel classes. Value must be a PHP array of valid datamodel classes. 
  * `custom_device_colors` Colors to used for custom classes. Value must be a PHP array with the class name as key and the text/background HTML color as values, see example below.

*Default values:*
```
'molkobain-datacenter-view-extended' => array(
    'enabled' => true,
    'debug' => false,
    'display_consistency_checks' => true,
    'enforce_consistency_checks' => false,
    'custom_device_classes' => array(),
    'custom_device_colors' => array(
        'ExampleClass' => array(
            'text' => '#fff',
            'background' => '#e87c1e',
        ),
    ),
),
```