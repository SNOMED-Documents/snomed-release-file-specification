# typeid (field)

A field in the Description and Relationship Release Files which contains a SNOMED CT identifier that represents the type of Description or Relationship represented.

* _Description.**typeId**_ represents the type of Description. Description types include subtypes of [900000000000446008 |Description type (core metadata concept)|](http://snomed.info/id/900000000000446008) . These include [900000000000013009 |Synonym (core metadata concept)|](http://snomed.info/id/900000000000013009) and [900000000000003001 |Fully specified name (core metadata concept)|](http://snomed.info/id/900000000000003001). There is no _typeId_ value for " Preferred term " as the preferred term is the synonym marked as "Preferred" in the appropriate [Language Reference Sets](broken-reference).
* _Relationship.**typeId**_ represents the type of Relationship between the concept identified by sourceId and the concept identified by destinatonId. Relationship types are [116680003 |Is a (attribute)|](http://snomed.info/id/116680003) and subtypes of [410662002 |Concept model attribute (attribute)|](http://snomed.info/id/410662002) .

Note: Field name in the [Description file](../d/description-file.md) and in the [Relationship file](../r/relationship-file.md).

## Related Links

* [Concept Enumerations for Description typeId](../../appendix-e-concept-enumerations/e3-concept-enumerations-for-description-typeid.md)
* [Concept Enumerations for Relationship typeId](../../appendix-e-concept-enumerations/e7-concept-enumerations-for-relationship-typeid.md)
* [Description file](../d/description-file.md)
* [Relationship file](../r/relationship-file.md)






<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&entry.1767247133=Release+File+Specification&entry.670899847=typeid%20%28field%29" class="button primary">Provide Feedback</a>
