<button onclick="history.back()">Back</button>

# Datamodel changes

The extension alters the standard datamodel, below is a summary of these modifications to help you integrate it with your own extensions.

_Note: The following includes datamodel changes from the simple version of the extension as well._

## Modified classes
### Location
#### Fields

| Code                    | Change type           | Description                            |
|-------------------------|-----------------------|----------------------------------------|
| locationtype_id         | Added (force)         | External key to `LocationType`         |
| parent_id               | Added (if not exists) | Hierarchical key to self (`Location`)  |
| locations_list          | Added (if not exists) | Linked set to child `Location` objects |
| accesspermissions_list  | Added (if not exists) | Linked set of access permissions       |

### FunctionalCI
#### Fields

| Code                    | Change type           | Description                            |
|-------------------------|-----------------------|----------------------------------------|
| accesspermissions_list  | Added (if not exists) | Linked set of access permissions       |

### Rack
#### Fields

| Code                  | Change type         | Description                                                                                                         |
|-----------------------|---------------------|---------------------------------------------------------------------------------------------------------------------|
| nb_u                  | Replaced (redefine) | Height in units (U)                                                                                                 |
| units_order           | Added (define)      | Whether the Us are ordered from bottom to top (regular) or from top to bottom (reverse)                             |
| occupancy_rate_f      | Added (define)      | Occupancy rate of the front panel. Note that obsolete elements are NOT included                                     |
| occupancy_rate_r      | Added (define)      | Occupancy rate of the rear panel. Note that obsolete elements are NOT included                                      |
| weight                | Added (define)      | Weight of the `Rack` itself                                                                                         |
| cumulated_weight      | Added (define)      | Weight of the `Rack`. Note that obsolete elements are NOT included                                                  |
| max_allowed_weight    | Added (define)      | Maximum weight allowed in this `Rack`, should either be from the `Rack` specs or the room specs                     |
| used_weight_capacity  | Added (define)      | Cumulated weight over max. allowed weight                                                                           |
| cumulated_power_input | Added (define)      | Total expected power consumption of all the elements. Note that obsolete elements are NOT included                  |
| contracted_power      | Added (define)      | Contracted power (kVA)                                                                                              |
| power_reading_value   | Added (define)      | Power reading (kVA)                                                                                                 |
| power_reading_date    | Added (define)      | Reading date                                                                                                        |
| power_reading_usage   | Added (define)      | Power reading (%)                                                                                                   |
| datacenterslot_list   | Added (define)      | All the `DatacenterSlot` of this `Rack`, either for misc. equipments (cables, patch panels, ...) or future elements |

#### Methods

| Name                          | Change type         | Description                                  |
|-------------------------------|---------------------|----------------------------------------------|
| GetInitialStateAttributeFlags | Added (define)      | Force some (computed) fields to be read-only |
| GetAttributeFlags             | Added (define)      | Force some (computed) fields to be read-only |

#### Presentation
The `details` zlist is completely redefined to propose a nice presentation.

### Enclosure
#### Fields

| Code                  | Change type         | Description                                                                                                                      |
|-----------------------|---------------------|----------------------------------------------------------------------------------------------------------------------------------|
| nb_u                  | Replaced (redefine) | Height in units (U)                                                                                                              |
| position_v            | Added (define)      | Vertical position (U) of the `Enclosure` in the `Rack` (Must be the bottom position, not top)                                        |
| position_p            | Added (define)      | `Enclosure` panel (or `Rack` panel if directly in it) the element is for                                                         |
| units_order           | Added (define)      | Whether the Us are ordered from bottom to top (regular) or from top to bottom (reverse)                                          |
| layout                | Added (define)      | Whether to display devices realistically on a grid each having its own width & height; or just simply the number of devices      |
| nb_cols               | Added (define)      | For 'Grid' layout only. The number of columns of the `Enclosure`'s grid. It will determine how many devices can fit side by side |
| occupancy_rate_f      | Added (define)      | Occupancy rate of the front panel. Note that obsolete elements are NOT included                                                  |
| occupancy_rate_r      | Added (define)      | Occupancy rate of the rear panel. Note that obsolete elements are NOT included                                                   |
| weight                | Added (define)      | Weight of the `Rack` itself                                                                                                      |
| cumulated_weight      | Added (define)      | Weight of the `Rack`. Note that obsolete elements are NOT included                                                               |
| cumulated_power_input | Added (define)      | Total expected power consumption of all the elements. Note that obsolete elements are NOT included                               |
| datacenterslot_list   | Added (define)      | All the `DatacenterSlot` of this `Rack`, either for misc. equipments (cables, patch panels, ...) or future elements              |

#### Methods

| Name                          | Change type         | Description                                  |
|-------------------------------|---------------------|----------------------------------------------|
| GetInitialStateAttributeFlags | Added (define)      | Force some (computed) fields to be read-only |
| GetAttributeFlags             | Added (define)      | Force some (computed) fields to be read-only |

#### Presentation
The `details` zlist is completely redefined to propose a nice presentation.

### DatacenterDevice
#### Fields

| Code                 | Change type         | Description                                                                                                                                               |
|----------------------|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| nb_u                 | Replaced (redefine) | Height in units (U)                                                                                                                                       |
| position_p           | Added (define)      | `Enclosure` panel (or `Rack` panel if directly in it) the element is for                                                                                  |
| position_v           | Added (define)      | Vertical position (U) of the device in the `Enclosure` (or `Rack` if mounted directly on int). (Must be the bottom position, not top)                    |
| position_h           | Added (define)      | Horizontal position of the device in its `Enclosure` (Must be the left side, not right). This ONLY applies if its `Enclosure`'s layout is set to 'Grid' |
| nb_cols              | Added (define)      | Width of of the device defined by on how many grid columns it spreads. This ONLY applies if its `Enclosure`'s layout is set to 'Grid'                     |
| zero_u               | Added (define)      | Only set to 'Yes' for devices that do not fit in standard racks / enclosures layout (eg. vertical PDU)                                                    |
| weight               | Added (define)      | Weight of the device itself                                                                                                                               |
| expected_power_input | Added (define)      | Expected power consumption of the device                                                                                                                  |

#### Presentation
The `details` zlist is completely redefined to propose a nice presentation.

### PDU
#### Fields

| Code         | Change type    | Description                                                                                                                                              |
|--------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| enclosure_id | Added (define) | `Enclosure` to which the `PDU` is attached to                                                                                                            |
| nb_u         | Added (define) | Height in units (U)                                                                                                                                      |
| position_v   | Added (define) | Vertical position (U) of the device in the enclosure (or rack if mounted directly on int). (Must be the bottom position, not top)                        |
| position_p   | Added (define) | `Enclosure` panel (or `Rack` panel if directly in it) the `PDU` is for                                                                                   |
| position_h   | Added (define) | Horizontal position of the `PDU` in its `Enclosure` (Must be the left side, not right). This ONLY applies if its `Enclosure`'s layout is set to 'Grid' |
| nb_cols      | Added (define) | Width of of the `PDU` defined by on how many grid columns it spreads. This ONLY applies if its `Enclosure`'s layout is set to 'Grid'                  |
| zero_u       | Added (define) | Only set to 'Yes' for devices that do not fit in standard racks / enclosures layout (eg. vertical PDU)                                                   |
| weight       | Added (define) | Weight of the `PDU` itself                                                                                                                               |

#### Presentation
The `details` zlist is completely redefined to propose a nice presentation.

## New classes
### LocationType

* Description: New typology to define the type of a `Location`, typically a room, a floor, a building, ...
* Parent: `Typology`

#### Fields

| Code           | Label     | Type               | Description                        |
|----------------|-----------|--------------------|------------------------------------|
| locations_list | Locations | AttributeLinkedSet | List of all locations of this type |

### DatacenterSlot

  * Description: Class to represent specific usage of datacenter hosts' slots (racks, enclosure), see derived classes.
  * Parent: `cmdbAbstractObject`

#### Fields

| Code                   | Label                    | Type                | Description                        |
|------------------------|--------------------------|---------------------|------------------------------------|
| name                   | Name                     | AttributeString     | Name                                                                                                                                                          |
| org_id                 | Organization             | AttributeExternalKey | Extenral key to the `Organization`                                                                                                                           |
| location_id            | Location                 | AttributeExternalKey | External key to the `Location`                                                                                                                               |
| rack_id                | Rack                     | AttributeExternalKey | External key to the `Rack`                                                                                                                                   |
| enclosure_id           | Enclosure                | AttributeExternalKey | External key to the `Enclosure`                                                                                                                              |
| position_p             | Panel                    | AttributeEnum        | `Enclosure` panel (or `Rack` panel if directly in it) the slot is for                                                                                        |
| position_v             | Vert. position           | AttributeMHFRackUnit | Vertical position (U) of the slot in the `Enclosure` (or `Rack` if mounted directly on int). (Must be the bottom position, not top)                          |
| position_h             | Hori. position           | AttributeInteger     | Horizontal position of the device in its `Enclosure` (Must be the left side, not right). This ONLY applies if its `Enclosure`'s layout is set to 'Grid' |
| nb_u                   | Height                   | AttributeMHFRackUnit | Height in units (U)                                                                                                                                          |
| nb_cols                | Width                    | AttributeInteger     | Width of the slot defined by on how many grid columns it spreads. This ONLY applies if its `Enclosure`'s layout is set to 'Grid'                             |
| weight                 | Weight (kg)              | AttributeDecimal     | Weight of the slot itself, will be used to compute cumulated weight of its host                                                                              |
| expected_power_input   | Expected consumption (W) | AttributeInteger     | Expected power consumption of the slot                                                                                                                       |
| description            | Description              | AttributeHTML        | Description of the slot usage                                                                                                                                |
| accesspermissions_list | Access permissions       | AttributeLinkedSet   | Access permissions for the slot                                                                                                                              |

### MiscEquipmentSlot

  * Description: Class to represent a slot where misc. equipements are stored (eg. a shelf with devices that don't fit the standard U form factor)
  * Parent: `DatacenterSlot`

### ReservedSlot

* Description: Class to represent a slot reserved for future device to set there
* Parent: `DatacenterSlot`

## Menus
### New menus

  * `Typology` menu: A badge dashlet is added in the first cell with ID `LocationType`. 