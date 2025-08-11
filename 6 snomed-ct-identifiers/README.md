# SNOMED CT Identifiers

SNOMED Clinical Terms Components are identified and referenced using numeric identifiers. These identifiers have the data type SCTID (SNOMED CT Identifier).

The SCTID data type is 64-bit integer which is allocated and represented in accordance with a set of rules. These rules enable each SCTID to refer unambiguously to a unique component. They also support separate partitions for allocation of Identifiers for particular types of component. In the case of components that originate in an Extension, the SCTID also supports separate namespaces that distinguish between different issuing organizations.

Details of the SCTID are described in the following sections:

* [SCTID Data Type](6.1-sctid-data-type.md)
* [SCTID Representation](6.2-sctid-representation.md)
* [SCTID Constraints](6.3-sctid-constraints.md)
* [Check-digit](<6.4 check-digit/>)
* [Partition Identifier](6.5-partition-identifier.md)
* [Namespace-Identifier](6.6-namespace-identifier.md)
* [Item-Identifier Digits](6.7-item-identifier-digits.md)
* [Example SNOMED CT identifiers](6.8-example-snomed-ct-identifiers.md)
* [The Namespace Hierarchy](6.9-the-namespace-hierarchy.md)
