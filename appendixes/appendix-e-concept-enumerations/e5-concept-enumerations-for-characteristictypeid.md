# E.5 Concept Enumerations for characteristicTypeId

This [concept enumeration](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept+enumeration "Glossary link: concept enumeration") enumeration represents a value that can be applied to the _relationship_.[characteristicTypeId](https://confluence.ihtsdotools.org/display/DOCRELFMT/characteristicTypeId+\(field\) "Reference term: characteristicTypeId \(field\)") field. This is used to indicate that a [relationship](https://confluence.ihtsdotools.org/display/DOCGLOSS/relationship "Glossary link: relationship") forms part of the definition of the source [concept](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept "Glossary link: concept").

[Table E.5-1](https://confluence.ihtsdotools.org/display/DOCRELFMT/E.5+Concept+Enumerations+for+characteristicTypeId#Table-chartype "Characteristic type \(core metadata concept\) \(900000000000449001\)") shows the current  set of values for this _concept enumeration_. 

Table E.5-1: Characteristic type (core metadata concept) (900000000000449001)

Concept| **Comment**  
---|---  
[ 900000000000006009 | Defining relationship|](http://snomed.info/id/900000000000006009 "900000000000006009 | Defining relationship |") | A general value which is a _supertype_ of [ 900000000000011006 | Inferred relationship|](http://snomed.info/id/900000000000011006 "900000000000011006 | Inferred relationship |") and [ 900000000000010007 | Stated relationship|](http://snomed.info/id/900000000000010007 "900000000000010007 | Stated relationship |") . This value is not applied to any released _relationships_.  
[ 900000000000011006 | Inferred relationship|](http://snomed.info/id/900000000000011006 "900000000000011006 | Inferred relationship |") | Indicates that this defining _relationship_ was inferred by a [description logic classifier](https://confluence.ihtsdotools.org/display/DOCGLOSS/description+logic+classifier "Glossary link: description logic classifier") from the [stated view](https://confluence.ihtsdotools.org/display/DOCGLOSS/stated+view "Glossary link: stated view") of the _concept definition_.  
**Obsolete values that are no longer used**|   
  
[ 900000000000010007 | Stated relationship|](http://snomed.info/id/900000000000010007 "900000000000010007 | Stated relationship |") | Indicates that this defining _relationship_ was stated by a terminology author.  
[ 900000000000225001 | Qualifying relationship|](http://snomed.info/id/900000000000225001 "900000000000225001 | Qualifying relationship |") | The _relationship_ is not part of the definition of the _concept_ but indicates a possible qualification that may be applied to refine a [postcoordinated expression](https://confluence.ihtsdotools.org/display/DOCGLOSS/postcoordinated+expression "Glossary link: postcoordinated expression") that refers to the source _concept_.  
[ 900000000000227009 | Additional relationship|](http://snomed.info/id/900000000000227009 "900000000000227009 | Additional relationship |") | The _relationship_ is not part of the definition of the _concept_ but is used to convey some additional information about the _concept_ . This additional information may only be applicable to a particular jurisdiction or use case.
