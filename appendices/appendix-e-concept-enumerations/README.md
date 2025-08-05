# Appendix E: Concept Enumerations

[SNOMED CT core](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT+core) _components_ have some fields that have values represented by [concepts](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept) in specific parts of the [SNOMED CT](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT) hierarchy. These are referred to as _concept_ enumerations.

The range of permitted values for each of the _concept_ enumerations is the set of [subtypes](https://confluence.ihtsdotools.org/display/DOCGLOSS/subtype) of a specified _concept_ which is itself a _subtype_ of [900000000000442005 | Core metadata concept (core metadata concept)|](http://snomed.info/id/900000000000442005) . The current set of _concept_ enumeration types is shown in [Table Appendix E:-1](../../display/DOCRELFMT/Appendix+E:+Concept+Enumerations/#Table-concept-table-core). The values of each of these and the ways they should be used in implemented systems are described in the following subsections.

Table Appendix E:thumbsdown: Core metadata concept (core metadata concept) (900000000000442005)

| **Concept**           | **Comment**                                 |
| --------------------- | ------------------------------------------- |
| \[ 900000000000443000 | Module (core metadata concept)              |
| \[ 900000000000444006 | Definition status (core metadata concept)   |
| \[ 900000000000446008 | Description type (core metadata concept)    |
| \[ 900000000000447004 | Case significance (core metadata concept)   |
| \[ 900000000000449001 | Characteristic type (core metadata concept) |
| \[ 900000000000450001 | Modifier (core metadata concept)            |
| \[ 900000000000453004 | Identifier scheme (core metadata concept)   |

Note: Many of the concept enumerations include values that significantly impact the meaning or use of a _component_. Therefore, implementers may find it necessary to partially hard-code the way their systems process particular values. In these cases, the _concept_ referenced by the value is only of value when there is a requirement to display a human readable rending of the value. The main exceptions to this are [900000000000443000 | Module (core metadata concept)|](http://snomed.info/id/900000000000443000) and [900000000000453004 | Identifier scheme (core metadata concept)|](http://snomed.info/id/900000000000453004) both of which represent extensible sets of values as new modules or alternative _identifier_ schemes may be added in local [Extensions](https://confluence.ihtsdotools.org/display/DOCGLOSS/Extension) .
