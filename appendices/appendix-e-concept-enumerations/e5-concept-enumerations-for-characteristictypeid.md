# E.5 Concept Enumerations for characteristicTypeId

This [concept enumeration](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept+enumeration) enumeration represents a value that can be applied to the _relationship_.[characteristicTypeId](https://confluence.ihtsdotools.org/display/DOCRELFMT/characteristicTypeId+\(field\)) field. This is used to indicate that a [relationship](https://confluence.ihtsdotools.org/display/DOCGLOSS/relationship) forms part of the definition of the source [concept](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept).

[Table E.5-1](https://confluence.ihtsdotools.org/display/DOCRELFMT/E.5+Concept+Enumerations+for+characteristicTypeId#Table-chartype) shows the current set of values for this _concept enumeration_.

Table E.5-1: Characteristic type (core metadata concept) (900000000000449001)

| Concept                                     | **Comment**           |
| ------------------------------------------- | --------------------- |
| \[ 900000000000006009                       | Defining relationship |
| \[ 900000000000011006                       | Inferred relationship |
| **Obsolete values that are no longer used** |                       |

[900000000000010007 | Stated relationship|](http://snomed.info/id/900000000000010007) | Indicates that this defining _relationship_ was stated by a terminology author.\
[900000000000225001 | Qualifying relationship|](http://snomed.info/id/900000000000225001) | The _relationship_ is not part of the definition of the _concept_ but indicates a possible qualification that may be applied to refine a [postcoordinated expression](https://confluence.ihtsdotools.org/display/DOCGLOSS/postcoordinated+expression) that refers to the source _concept_.\
[900000000000227009 | Additional relationship|](http://snomed.info/id/900000000000227009) | The _relationship_ is not part of the definition of the _concept_ but is used to convey some additional information about the _concept_ . This additional information may only be applicable to a particular jurisdiction or use case.
