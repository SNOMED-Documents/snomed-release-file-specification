# 5.2 Reference Set Types

This section describes four categories of [reference set](https://confluence.ihtsdotools.org/display/DOCGLOSS/reference+set "Glossary link: reference set") types, each of which contain several sub-types.

  * [5.2.1 Content Reference Sets](5.2.1-Content-Reference-Sets_142120941.html)
    * [4.2.2. Ordered Component Reference Set](4.2.2.-Ordered-Component-Reference-Set_45529890.html)
    * [5.2.1.1 Simple Reference Set](5.2.1.1-Simple-Reference-Set_28739370.html)
    * [5.2.1.3 Attribute Value Reference Set](5.2.1.3-Attribute-Value-Reference-Set_28739372.html)
      * [5.2.3.1 Component Inactivation Reference Sets](5.2.3.1-Component-Inactivation-Reference-Sets_106699850.html)
    * [5.2.1.4 Association Reference Set](5.2.1.4-Association-Reference-Set_28739378.html)
      * [5.2.5.1 Historical Association Reference Sets](5.2.5.1-Historical-Association-Reference-Sets_106693955.html)
    * [5.2.1.5 Ordered Association Reference Set](5.2.1.5-Ordered-Association-Reference-Set_45529892.html)
    * [5.2.1.6 DEPRECATED: Annotation Reference Set](28739377.html)
    * [5.2.1.7 Query Specification Reference Set](5.2.1.7-Query-Specification-Reference-Set_28739376.html)
    * [5.2.1.8 Ordered Reference Set](5.2.1.8-Ordered-Reference-Set_28739371.html)
    * [5.2.1.9 OWL Expression Reference Set](5.2.1.9-OWL-Expression-Reference-Set_66486617.html)
    * [5.2.1.10 Postcoordinated Expression Type Reference Set](5.2.1.10--Postcoordinated-Expression-Type-Reference-Set_142120942.html)
  * [5.2.2 Language Reference Sets](5.2.2-Language-Reference-Sets_142120944.html)
    * [5.2.2.1 Language Reference Set](5.2.2.1-Language-Reference-Set_28739375.html)
  * [5.2.3 Map Reference Sets](5.2.3-Map-Reference-Sets_142120945.html)
    * [5.2.3.1 Simple Map from SNOMED CT Reference Set](5.2.3.1-Simple-Map-from-SNOMED-CT-Reference-Set_142120946.html)
    * [5.2.3.2 Simple Map to SNOMED CT Reference Set](5.2.3.2-Simple-Map-to-SNOMED-CT-Reference-Set_142120947.html)
    * [5.2.3.3 Complex and Extended Map from SNOMED CT Reference Sets](5.2.3.3-Complex-and-Extended-Map-from-SNOMED-CT-Reference-Sets_28739374.html)
    * [5.2.3.4 Map to SNOMED CT with Correlation and Origin Reference Set](5.2.3.4-Map-to-SNOMED-CT-with-Correlation-and-Origin-Reference-Set_38260134.html)
    * [5.2.3.5 Code to Expression Reference Set](5.2.3.5-Code-to-Expression-Reference-Set_38259887.html)
    * [5.2.3.6 Simple map with correlation from SNOMED CT type reference set](5.2.3.6-Simple-map-with-correlation-from-SNOMED-CT-type-reference-set_142120948.html)
    * [5.2.3.7 Simple map with correlation to SNOMED CT type reference set](5.2.3.7-Simple-map-with-correlation-to-SNOMED-CT-type-reference-set_142120949.html)
    * [5.2.3.8 Simple map with correlation from SNOMED CT to SNOMED CT type reference set](5.2.3.8-Simple-map-with-correlation-from-SNOMED-CT-to-SNOMED-CT-type-reference-set_142119867.html)
  * [5.2.4 Metadata Reference Sets](5.2.4-Metadata-Reference-Sets_142120950.html)
    * [5.2.4.1 Reference Set Descriptor](5.2.4.1-Reference-Set-Descriptor_28739369.html)
    * [5.2.4.2 Module Dependency Reference Set](5.2.4.2-Module-Dependency-Reference-Set_28739379.html)
    * [5.2.4.3 Description Format Reference Set](5.2.4.3-Description-Format-Reference-Set_28739380.html)
    * [5.2.4.4 MRCM Domain Reference Set](5.2.4.4-MRCM-Domain-Reference-Set_45529893.html)
    * [5.2.4.5 MRCM Attribute Domain Reference Set](5.2.4.5-MRCM-Attribute-Domain-Reference-Set_45529894.html)
    * [5.2.4.6 MRCM Attribute Range Reference Set](5.2.4.6-MRCM-Attribute-Range-Reference-Set_45529895.html)
    * [5.2.4.7 MRCM Module Scope Reference Set](5.2.4.7-MRCM-Module-Scope-Reference-Set_45529896.html)
    * [5.2.4.8 Component Annotation String Value Reference Set](5.2.4.8-Component-Annotation-String-Value-Reference-Set_212339752.html)
    * [5.2.4.9 Member Annotation String Value Reference Set](5.2.4.9-Member-Annotation-String-Value-Reference-Set_212339754.html)

Each reference set type follows a pattern and that pattern is also represented in a machine readable form using a set of [Reference Set Descriptor](5.2.4.1-Reference-Set-Descriptor_28739369.html) members (known as a Descriptor Template, for short). In most case, the same pattern may be used to define a number of different [reference sets](https://confluence.ihtsdotools.org/display/DOCGLOSS/reference+set "Glossary link: reference sets") to serve a variety of purposes. However, there are also some highly specific [reference set](https://confluence.ihtsdotools.org/display/DOCGLOSS/reference+set "Glossary link: reference set") types that exist for a single specified purpose. These are the [Reference Set Descriptor Reference Set](5.2.4.1-Reference-Set-Descriptor_28739369.html), [Module Dependency Reference Set](5.2.4.2-Module-Dependency-Reference-Set_28739379.html) and [Description Format Reference Set](5.2.4.3-Description-Format-Reference-Set_28739380.html).

In each subsection, a [reference set](https://confluence.ihtsdotools.org/display/DOCGLOSS/reference+set "Glossary link: reference set") type is described under the following subheadings:

  * The purpose of the [reference set](https://confluence.ihtsdotools.org/display/DOCGLOSS/reference+set "Glossary link: reference set");

  * The format of the [reference set](https://confluence.ihtsdotools.org/display/DOCGLOSS/reference+set "Glossary link: reference set") member record is detailed in a table;

  * The metadata supporting the [reference set](https://confluence.ihtsdotools.org/display/DOCGLOSS/reference+set "Glossary link: reference set");

  * The machine readable [reference set](https://confluence.ihtsdotools.org/display/DOCGLOSS/reference+set "Glossary link: reference set") descriptor member records for the [reference set](https://confluence.ihtsdotools.org/display/DOCGLOSS/reference+set "Glossary link: reference set") type;

  * Examples of the [reference set](https://confluence.ihtsdotools.org/display/DOCGLOSS/reference+set "Glossary link: reference set") type;

Related Links

  * [Unicode UTF-8 encoding](Appendix-C.-Unicode-UTF-8-encoding_33490103.html)
  * [Reference set](https://confluence.ihtsdotools.org/display/DOCGLOSS/Reference+set "Glossary link: Reference set")

