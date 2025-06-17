# typeid-field

## typeId (field)

A field in the [Description](https://confluence.ihtsdotools.org/display/DOCGLOSS/Description) and [Relationship](https://confluence.ihtsdotools.org/display/DOCGLOSS/Relationship) [Release Files](https://confluence.ihtsdotools.org/display/DOCGLOSS/Release+File) which contains a [SNOMED CT identifier](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT+identifier) that represents the type of [Description](https://confluence.ihtsdotools.org/display/DOCGLOSS/Description) or [Relationship](https://confluence.ihtsdotools.org/display/DOCGLOSS/Relationship) represented.

* [_Description_](https://confluence.ihtsdotools.org/display/DOCGLOSS/Description) _.**typeId**_ represents the type of [Description](https://confluence.ihtsdotools.org/display/DOCGLOSS/Description). [Description](https://confluence.ihtsdotools.org/display/DOCGLOSS/Description) types include [subtypes](https://confluence.ihtsdotools.org/display/DOCGLOSS/subtype) of [900000000000446008 | Description type (core metadata concept)|](http://snomed.info/id/900000000000446008) . These include [900000000000013009 | Synonym (core metadata concept)|](http://snomed.info/id/900000000000013009) and [900000000000003001 | Fully specified name (core metadata concept)|](http://snomed.info/id/900000000000003001) . There is no _typeId_ value for " [Preferred term](https://confluence.ihtsdotools.org/display/DOCGLOSS/Preferred+term) " as the [preferred term](https://confluence.ihtsdotools.org/display/DOCGLOSS/preferred+term) is the [synonym](https://confluence.ihtsdotools.org/display/DOCGLOSS/synonym) marked as "Preferred" in the appropriate \[see [4.2.1 Language Reference Sets](../../../../pages/createpage.action) ].
* [_Relationship_](https://confluence.ihtsdotools.org/display/DOCGLOSS/Relationship) _.**typeId**_ represents the type of [Relationship](https://confluence.ihtsdotools.org/display/DOCGLOSS/Relationship) between the [concept](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept) identified by [sourceId](https://confluence.ihtsdotools.org/display/DOCGLOSS/sourceId) and the [concept](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept) identified by destinatonId. [Relationship types](https://confluence.ihtsdotools.org/display/DOCGLOSS/Relationship+type) are [116680003 | Is a (attribute)|](http://snomed.info/id/116680003) and [subtypes](https://confluence.ihtsdotools.org/display/DOCGLOSS/subtype) of [410662002 | Concept model attribute (attribute)|](http://snomed.info/id/410662002) .

Note: Field name in the [Description file](https://confluence.ihtsdotools.org/display/DOCGLOSS/Description+file) and in the [Relationship file](https://confluence.ihtsdotools.org/display/DOCGLOSS/Relationship+file) .

## Related Links

* [Concept Enumerations for Description typeId](../../../../pages/createpage.action)
* [Concept Enumerations for Relationship typeId](../../../../pages/createpage.action)
* [Concept model attribute](https://confluence.ihtsdotools.org/display/DOCGLOSS/Concept+model+attribute)
* [Description](https://confluence.ihtsdotools.org/display/DOCRELFMT/Description+file)
* [Relationship](https://confluence.ihtsdotools.org/display/DOCRELFMT/Relationship+file)
