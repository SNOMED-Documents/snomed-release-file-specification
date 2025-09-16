# Reference Set Types

This section describes four categories of reference set types, each of which contain several sub-types.

* [Content Reference Sets](<5.2.1 content-reference-sets/>)
  * [Simple Reference Set](<5.2.1 content-reference-sets/5.2.1.1-simple-reference-set.md>)
  * [Attribute Value Reference Set](../../5-reference-set-release-files-specification/5.2-reference-set-types/5.2.1-content-reference-sets/5.2.1.3-attribute-value-reference-set/)
    * [Component Inactivation Reference Sets](../../5-reference-set-release-files-specification/5.2-reference-set-types/5.2.1-content-reference-sets/5.2.1.3-attribute-value-reference-set/5.2.1.3-attribute-value-reference-set.md)
  * [Association Reference Set](../../5-reference-set-release-files-specification/5.2-reference-set-types/5.2.1-content-reference-sets/5.2.1.4-association-reference-set/)
    * [Historical Association Reference Sets](../../5-reference-set-release-files-specification/5.2-reference-set-types/5.2.1-content-reference-sets/5.2.1.4-association-reference-set/5.2.5.1-historical-association-reference-sets.md)
  * [DEPRECATED: Annotation Reference Set](<5.2.1 content-reference-sets/5.2.1.6-deprecated-annotation-reference-set.md>)
  * [Query Specification Reference Set](<5.2.1 content-reference-sets/5.2.1.7-query-specification-reference-set.md>)
  * [DEPRECATED: Ordered Reference Set](../../5-reference-set-release-files-specification/5.2-reference-set-types/5.2.1-content-reference-sets/5.2.1.8-ordered-reference-set/)
    * [Ordered Component Reference Set](../../5-reference-set-release-files-specification/5.2-reference-set-types/5.2.1-content-reference-sets/5.2.1.8-ordered-reference-set/5.2.1.5-ordered-association-reference-set-1.md)
    * [Ordered Association Reference Set](../../5-reference-set-release-files-specification/5.2-reference-set-types/5.2.1-content-reference-sets/5.2.1.8-ordered-reference-set/5.2.1.5-ordered-association-reference-set.md)
  * [OWL Expression Reference Set](<5.2.1 content-reference-sets/5.2.1.9-owl-expression-reference-set.md>)
  * [Postcoordinated Expression Type Reference Set](<5.2.1 content-reference-sets/5.2.1.10-postcoordinated-expression-type-reference-set.md>)
* [Language Reference Sets](../../reference-set-release-file-specification/5.2-reference-set-types/5.2.2.1-language-reference-set.md)
  * [Language Reference Set](../../reference-set-release-file-specification/5.2-reference-set-types/5.2.2.1-language-reference-set.md)
* [Map Reference Sets](<5.2.3 map-reference-sets/>)
  * [Simple Map from SNOMED CT Reference Set](../../5-reference-set-release-files-specification/5.2-reference-set-types/5.2.3-map-reference-sets/5.2.3.1-simple-map-from-snomed-ct-reference-set.md)
  * [Simple Map to SNOMED CT Reference Set](<5.2.3 map-reference-sets/5.2.3.2-simple-map-to-snomed-ct-reference-set.md>)
  * [Complex and Extended Map from SNOMED CT Reference Sets](<5.2.3 map-reference-sets/5.2.3.3-complex-and-extended-map-from-snomed-ct-reference-sets.md>)
  * [Map to SNOMED CT with Correlation and Origin Reference Set](<5.2.3 map-reference-sets/5.2.3.4-map-to-snomed-ct-with-correlation-and-origin-reference-set.md>)
  * [Code to Expression Reference Set](<5.2.3 map-reference-sets/5.2.3.5-code-to-expression-reference-set.md>)
  * [Simple map with correlation from SNOMED CT type reference set](<5.2.3 map-reference-sets/5.2.3.6-simple-map-with-correlation-from-snomed-ct-type-reference-set.md>)
  * [Simple map with correlation to SNOMED CT type reference set](<5.2.3 map-reference-sets/5.2.3.7-simple-map-with-correlation-to-snomed-ct-type-reference-set.md>)
  * [Simple map with correlation from SNOMED CT to SNOMED CT type reference set](<5.2.3 map-reference-sets/5.2.3.8-simple-map-with-correlation-from-snomed-ct-to-snomed-ct-type-reference-set.md>)
* [Metadata Reference Sets](<5.2.4 metadata-reference-sets/>)
  * [Reference Set Descriptor](<5.2.4 metadata-reference-sets/5.2.4.1-reference-set-descriptor.md>)
  * [Module Dependency Reference Set](<5.2.4 metadata-reference-sets/5.2.4.2-module-dependency-reference-set.md>)
  * [Description Format Reference Set](<5.2.4 metadata-reference-sets/5.2.4.3-description-format-reference-set.md>)
  * [MRCM Domain Reference Set](<5.2.4 metadata-reference-sets/5.2.4.4-mrcm-domain-reference-set.md>)
  * [MRCM Attribute Domain Reference Set](<5.2.4 metadata-reference-sets/5.2.4.5-mrcm-attribute-domain-reference-set.md>)
  * [MRCM Attribute Range Reference Set](<5.2.4 metadata-reference-sets/5.2.4.6-mrcm-attribute-range-reference-set.md>)
  * [MRCM Module Scope Reference Set](<5.2.4 metadata-reference-sets/5.2.4.7-mrcm-module-scope-reference-set.md>)
  * [Component Annotation String Value Reference Set](<5.2.4 metadata-reference-sets/5.2.4.8-component-annotation-string-value-reference-set.md>)
  * [Member Annotation String Value Reference Set](<5.2.4 metadata-reference-sets/5.2.4.9-member-annotation-string-value-reference-set.md>)

Each reference set type follows a pattern and that pattern is also represented in a machine readable form using a set of [Reference Set Descriptor ](<5.2.4 metadata-reference-sets/5.2.4.1-reference-set-descriptor.md>)members (known as a Descriptor Template, for short). In most case, the same pattern may be used to define a number of different reference sets to serve a variety of purposes. However, there are also some highly specific reference set types that exist for a single specified purpose. These are the [Reference Set Descriptor Reference Set](<5.2.4 metadata-reference-sets/5.2.4.1-reference-set-descriptor.md>), [Module Dependency Reference Set ](<5.2.4 metadata-reference-sets/5.2.4.2-module-dependency-reference-set.md>)and [Description Format Reference Set](<5.2.4 metadata-reference-sets/5.2.4.3-description-format-reference-set.md>).

In each subsection, a reference set type is described under the following subheadings:

* The purpose of the reference set;
* The format of the reference set member record is detailed in a table;
* The metadata supporting the reference set;
* The machine readable reference set descriptor member records for the reference set type;
* Examples of the reference set type;

Related Links

* [Unicode UTF-8 encoding](../../appendices/appendix-c-unicode-utf-8-encoding.md)









<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&entry.1767247133=Release+File+Specification&entry.670899847=Reference%20Set%20Types" class="button primary">Provide Feedback</a>
