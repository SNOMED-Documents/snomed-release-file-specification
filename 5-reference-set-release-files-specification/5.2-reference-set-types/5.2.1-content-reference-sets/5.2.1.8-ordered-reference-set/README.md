# Ordered Reference Set

{% hint style="danger" %}
**Deprecation Notice**

The Ordered Reference Set pattern is now **deprecated** as it has been replaced with two reference set types each of which is specific to one of the two distinct use cases supported by the Ordered Reference set pattern.

The recommended Reference sets to address the purposes identified below are now:

* [Ordered Component Reference Set](5.2.1.5-ordered-association-reference-set-1.md)
  * This allows an ordered or prioritized list of components to be represented.
  * It omits the **linkedToId** field in the pattern shown below as this is not required to address this use case.
* [Ordered Association Reference Set](5.2.1.5-ordered-association-reference-set.md)
  * This enables representation of alternative navigation hierarchies (in which child concepts are ordered) and also also supports representation of groups of ordered components.
  * The **linkedToId** field in the pattern shown below is replaced by the targetComponentId (this name is used to align with the [Association Reference Set ](../5.2.1.4-association-reference-set/)(used from unordered associations).

**Deprecation does not prevent continued use of an existing reference set pattern**. However it does indicate that a different solution is now specified and recommended to meet the requirements for this pattern
{% endhint %}

## Purpose

An [447258008 |Ordered type reference set|](http://snomed.info/id/447258008) allows a collection of components to be defined with a specified given a priority ordering. This type of reference ret can also be used to specify ordered associations between different components. These can be used to specify several interrelated subsets of components and to define alternative hierarchies for navigation and selection of concepts or descriptions.

## Data structure

An Ordered Reference Set is an Integer Component Reference Set used to represent ordered lists and alternative hierarchies. Its structure is shown in the following table.

Table 5.2.1.8-1: Ordered reference set - Data structure



## Metadata

The following metadata in the "Foundation metadata [concept](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept)" [hierarchy](https://confluence.ihtsdotools.org/display/DOCGLOSS/hierarchy) supports this [reference set](https://confluence.ihtsdotools.org/display/DOCGLOSS/reference+set)

Table 5.2.1.8-2: Ordered References Sets in the Metadata Hierarchy

* [900000000000454005 | Foundation metadata concept|](http://snomed.info/id/900000000000454005)
  * [900000000000455006 | Reference set|](http://snomed.info/id/900000000000455006)
    * [447258008 | Ordered type reference set|](http://snomed.info/id/447258008)

## Reference Set Descriptor and Example Data

### Descriptor Template

The tables below show the descriptor that defines the structure of the [447258008 | Ordered type reference set|](http://snomed.info/id/447258008) pattern and an example of descriptor for a [reference set](https://confluence.ihtsdotools.org/display/DOCGLOSS/reference+set) that follows this pattern.

Table 5.2.1.8-3: Refset Descriptor rows for Ordered Reference Set

| **refsetId**          | **referencedComponentId** | **attributeDescription**                                        | **attributeType**        | **attributeOrder** |
| --------------------- | ------------------------- | --------------------------------------------------------------- | ------------------------ | ------------------ |
| \[ 900000000000456007 | Reference set descriptor  | ]\(http://snomed.info/id/900000000000456007 "900000000000456007 | Reference set descriptor | ")                 |
| \[ 900000000000456007 | Reference set descriptor  | ]\(http://snomed.info/id/900000000000456007 "900000000000456007 | Reference set descriptor | ")                 |
| \[ 900000000000456007 | Reference set descriptor  | ]\(http://snomed.info/id/900000000000456007 "900000000000456007 | Reference set descriptor | ")                 |

## Example Data

Table 5.2.1.8-4: Sample Content for an Ordered Reference Set

| **refsetId** | **referencedComponentId (Referenced component)**               | **order (Attribute order)**                   | **linkedTo ("Linked to" reference set attribute)**             |
| ------------ | -------------------------------------------------------------- | --------------------------------------------- | -------------------------------------------------------------- |
| \[ 447570008 | SNOMED CT top level navigation hierarchy ordered reference set | ]\(http://snomed.info/id/447570008 "447570008 | SNOMED CT top level navigation hierarchy ordered reference set |
| \[ 447570008 | SNOMED CT top level navigation hierarchy ordered reference set | ]\(http://snomed.info/id/447570008 "447570008 | SNOMED CT top level navigation hierarchy ordered reference set |
| \[ 447570008 | SNOMED CT top level navigation hierarchy ordered reference set | ]\(http://snomed.info/id/447570008 "447570008 | SNOMED CT top level navigation hierarchy ordered reference set |
| \[ 447570008 | SNOMED CT top level navigation hierarchy ordered reference set | ]\(http://snomed.info/id/447570008 "447570008 | SNOMED CT top level navigation hierarchy ordered reference set |
| \[ 447570008 | SNOMED CT top level navigation hierarchy ordered reference set | ]\(http://snomed.info/id/447570008 "447570008 | SNOMED CT top level navigation hierarchy ordered reference set |
| \[ 447570008 | SNOMED CT top level navigation hierarchy ordered reference set | ]\(http://snomed.info/id/447570008 "447570008 | SNOMED CT top level navigation hierarchy ordered reference set |
| \[ 447570008 | SNOMED CT top level navigation hierarchy ordered reference set | ]\(http://snomed.info/id/447570008 "447570008 | SNOMED CT top level navigation hierarchy ordered reference set |
| \[ 447570008 | SNOMED CT top level navigation hierarchy ordered reference set | ]\(http://snomed.info/id/447570008 "447570008 | SNOMED CT top level navigation hierarchy ordered reference set |
| \[ 447570008 | SNOMED CT top level navigation hierarchy ordered reference set | ]\(http://snomed.info/id/447570008 "447570008 | SNOMED CT top level navigation hierarchy ordered reference set |
| \[ 447570008 | SNOMED CT top level navigation hierarchy ordered reference set | ]\(http://snomed.info/id/447570008 "447570008 | SNOMED CT top level navigation hierarchy ordered reference set |
