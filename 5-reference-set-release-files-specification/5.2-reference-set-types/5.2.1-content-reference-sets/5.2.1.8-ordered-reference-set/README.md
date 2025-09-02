# DEPRECATED: Ordered Reference Set

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

**Ordered reference set - Data structure**

<table data-full-width="true"><thead><tr><th width="208.56640625">Field</th><th width="99.15234375">Data type</th><th width="620.0015869140625">Purpose</th><th width="89.484375">Mutable</th><th>PK*</th></tr></thead><tbody><tr><td>id</td><td>UUID</td><td>A 128 bit unsigned Integer, uniquely identifying this reference set member.Different versions of a <em>reference set member</em> share the same id but have different effectiveTime. This allows a <em>reference set member</em> to be modified or made inactive (i.e. removed from the active set) at a specified time.</td><td><mark style="color:$danger;"><strong>NO</strong></mark></td><td><mark style="color:$success;"><strong>YES</strong></mark><br>(Full/Snapshot)</td></tr><tr><td>effectiveTime</td><td>Time</td><td><p>The inclusive date or time at which this version of the identified reference set member became the current version.</p><p><strong>Note</strong> : In distribution files the effectiveTime should follow the short ISO date format (<em>YYYYMM DD</em>) and should not include the hours, minutes, seconds or timezone indicator.The current version of this reference set member at time <em>T</em> is the version with the most recent effectiveTime prior to or equal to time <em>T</em>.</p></td><td><mark style="color:$success;"><strong>YES</strong></mark></td><td><mark style="color:$success;"><strong>YES</strong></mark> <br>(Full)<br><mark style="color:$success;">Optional</mark> (Snapshot)</td></tr><tr><td>active</td><td>Boolean</td><td>The state of the identified reference set member as at the specified effectiveTime. If active = 1 (true) the reference set member is part of the current version of the set, if active = 0 (false) the reference set member is not part of the current version of the set.</td><td><mark style="color:$success;"><strong>YES</strong></mark></td><td><mark style="color:$danger;"><strong>NO</strong></mark></td></tr><tr><td>moduleId</td><td>SCTID</td><td><p>Identifies the SNOMED CT module that contains this reference set member as at the specified effectiveTime .</p><p>The value must be a subtype of <a href="http://snomed.info/id/900000000000443000">900000000000443000 |Module (core metadata concept)|</a> within the metadata hierarchy.</p></td><td><mark style="color:$success;"><strong>YES</strong></mark></td><td><mark style="color:$danger;"><strong>NO</strong></mark></td></tr><tr><td>refsetId</td><td>SCTID</td><td><p>Identifies the reference set to which this reference set member belongs.</p><p>A subtype descendant of:</p><p><a href="http://snomed.info/id/447258008">447258008 | Ordered type reference set|</a></p></td><td><mark style="color:$danger;"><strong>NO</strong></mark></td><td><mark style="color:$danger;"><strong>NO</strong></mark></td></tr><tr><td>referencedComponentId</td><td>SCTID</td><td>A reference to the SNOMED CT component to be included in the reference set.</td><td><mark style="color:$danger;"><strong>NO</strong></mark></td><td><mark style="color:$danger;"><strong>NO</strong></mark></td></tr><tr><td>order</td><td>Integer</td><td><p>Specifies the sort order of the list. The list is ordered by applying an ascending sort of the order value.</p><p>The value of order =1 represents the highest priority. A value of '0' is not allowed. Duplicate values are permitted and the sort order between two members with the same order value is not defined.</p><p>If the linkedToId value is not 0, sorting occurs within subgroups that share the same linkedToId.</p><p>Note: The name "order" is a reserved word in some database environments. Please consider this when using this column.</p></td><td><mark style="color:$success;"><strong>YES</strong></mark></td><td><mark style="color:$danger;"><strong>NO</strong></mark></td></tr><tr><td>linkedToId</td><td>SCTID</td><td><p>The identifier of a SNOMED CT component that acts as a grouper or hierarchy node, collecting together a subgroup from within the list.</p><p>This field either enables reference set member linked into a number of subgroups. These subgroups can be nested allowing representation of alternative hierarchies.</p><p>To link members into a subgroup, all components in the same subgroup should reference the same component. This can either be a component that represents the name of that subgroup or the first member of the subgroup. In the latter case, the first row of each subgroup will contain the same identifier in referencedComponentId and linkedToId and with order =1.</p><p>To link a number of children concepts to a single parent concept, one member record should exist per child, with the referencedComponentId field referencing the parent and this field referencing the child concept. The order field is then used to order the children concepts under the parent concept.</p><p>For ordered lists that do not require grouping or hierarchical arrangement the value of linkedToId should be the digit zero (0).</p></td><td><mark style="color:$success;"><strong>YES</strong></mark></td><td><mark style="color:$danger;"><strong>NO</strong></mark></td></tr></tbody></table>

***

## Metadata

The following metadata in the "Foundation metadata concept" hierarchy supports this reference set.

**Ordered References Sets in the Metadata Hierarchy**

> [900000000000454005 |Foundation metadata concept|](http://snomed.info/id/900000000000454005) &#x20;
>
> &#x20;    [900000000000455006 |Reference set|](http://snomed.info/id/900000000000455006) &#x20;
>
> &#x20;             [447258008 | Ordered type reference set|](http://snomed.info/id/447258008)

## Reference Set Descriptor and Example Data

{% hint style="info" %}
**Notes on the tables used to show descriptors and examples**

The reference set example tables on this page have been revised as follows to aid clarity and understanding:

* The first four columns which are present in all release files are not shown. The omitted columns (id, effectiveTime, active, moduleId) are used in the same way in all referenced sets to support identification, versioning and packaging. They do not directly affect the specific features of a particular reference set or reference set type.
* Reference set columns that contain SNOMED CT identifiers are expanded to show details of the concept or description referenced by that identifier. In some cases, the term is shown in the same column using the expression syntax, in other cases an additional column with a name suffix '\_term' has been added. In the standard reference set files only the identifier is present in the column and there is no added column for the term. When using reference sets, the term and other details of the component are looked up from the relevant component release files.
{% endhint %}

#### Descriptor Template

The tables below show the descriptor that defines the structure of the [|Ordered type reference set|](http://snomed.info/id/447258008) pattern and an example of descriptor for a reference set that follows this pattern.

**Refset Descriptor rows for Ordered Reference Set**

<table data-full-width="true"><thead><tr><th>refsetId</th><th>referencedComponentId </th><th>attributeDescription</th><th>attributeType</th><th>attributeOrder </th></tr></thead><tbody><tr><td><a href="http://snomed.info/id/900000000000456007">900000000000456007 |Reference set descriptor|</a></td><td><a href="http://snomed.info/id/447258008">447258008 |Ordered type reference set|</a><br><br></td><td><a href="http://snomed.info/id/449608002">449608002 |Referenced component|</a></td><td><a href="http://snomed.info/id/900000000000460005">900000000000460005 | Component type|</a></td><td>0</td></tr><tr><td><a href="http://snomed.info/id/900000000000456007">900000000000456007 |Reference set descriptor|</a></td><td><a href="http://snomed.info/id/447258008">447258008 |Ordered type reference set|</a></td><td><a href="http://snomed.info/id/447255006">447255006 |Priority order reference set attribute|</a></td><td><a href="http://snomed.info/id/900000000000478000">900000000000478000 | Unsigned integer|</a></td><td>1</td></tr><tr><td><a href="http://snomed.info/id/900000000000456007">900000000000456007 |Reference set descriptor|</a></td><td><a href="http://snomed.info/id/447258008">447258008 |Ordered type reference set|</a></td><td><a href="http://snomed.info/id/447257003">447257003 |"Linked to" reference set attribute|</a></td><td><a href="http://snomed.info/id/900000000000460005">900000000000460005 |Component type|</a></td><td>2</td></tr></tbody></table>

***

#### Example&#x20;

**Sample Content for an Ordered Reference Set**

<table data-full-width="true"><thead><tr><th width="384.71405029296875">refsetId</th><th width="213.87109375">referencedComponentId (Referenced component)</th><th width="151.65234375">order  (Attribute order)</th><th width="286.606201171875">linkedTo  ("Linked to" reference set attribute)</th></tr></thead><tbody><tr><td><a href="http://snomed.info/id/447570008">447570008 |SNOMED CT top level navigation hierarchy ordered reference set|</a></td><td><a href="http://snomed.info/id/64572001">64572001 |Disease|</a></td><td>1</td><td><a href="http://snomed.info/id/123946008">123946008 |Disorder by body site|</a><br></td></tr><tr><td><a href="http://snomed.info/id/447570008">447570008 |SNOMED CT top level navigation hierarchy ordered reference set|</a></td><td><a href="http://snomed.info/id/64572001">64572001 |Disease|</a></td><td>2</td><td><a href="http://snomed.info/id/370117001">370117001 |Disorder of system|</a></td></tr><tr><td><a href="http://snomed.info/id/447570008">447570008 |SNOMED CT top level navigation hierarchy ordered reference set|</a></td><td><a href="http://snomed.info/id/64572001">64572001 |Disease|</a></td><td>3</td><td><a href="http://snomed.info/id/278919001">278919001 |Communication disorder|</a></td></tr><tr><td><a href="http://snomed.info/id/447570008">447570008 |SNOMED CT top level navigation hierarchy ordered reference set|</a></td><td><a href="http://snomed.info/id/64572001">64572001 |Disease|</a></td><td>4</td><td><a href="http://snomed.info/id/74732009">74732009 |Mental disorder|</a></td></tr><tr><td><a href="http://snomed.info/id/447570008">447570008 |SNOMED CT top level navigation hierarchy ordered reference set|</a></td><td><a href="http://snomed.info/id/64572001">64572001 |Disease|</a></td><td>5</td><td><a href="http://snomed.info/id/39898005">39898005 |Sleep disorder|</a></td></tr><tr><td><a href="http://snomed.info/id/447570008">447570008 |SNOMED CT top level navigation hierarchy ordered reference set|</a></td><td><a href="http://snomed.info/id/64572001">64572001 |Disease|</a></td><td>6</td><td><a href="http://snomed.info/id/370118006">370118006 |Disorder of pregnancy / labor / delivery / puerperium|</a></td></tr><tr><td><a href="http://snomed.info/id/447570008">447570008 |SNOMED CT top level navigation hierarchy ordered reference set|</a></td><td><a href="http://snomed.info/id/64572001">64572001 |Disease|</a></td><td>7</td><td><a href="http://snomed.info/id/370119003">370119003 |Fetal / neonatal / perinatal disorder|</a></td></tr><tr><td><a href="http://snomed.info/id/447570008">447570008 |SNOMED CT top level navigation hierarchy ordered reference set|</a></td><td><a href="http://snomed.info/id/64572001">64572001 |Disease|</a></td><td>8</td><td><a href="http://snomed.info/id/370120009">370120009 |Endocrine / nutritional / metabolic disorder|</a></td></tr><tr><td><a href="http://snomed.info/id/447570008">447570008 |SNOMED CT top level navigation hierarchy ordered reference set|</a></td><td><a href="http://snomed.info/id/64572001">64572001 |Disease|</a></td><td>9</td><td><a href="http://snomed.info/id/370121008">370121008 |Disorder of blood / lymphatics / immune system|</a></td></tr><tr><td><a href="http://snomed.info/id/447570008">447570008 |SNOMED CT top level navigation hierarchy ordered reference set|</a></td><td><a href="http://snomed.info/id/64572001">64572001 |Disease|</a></td><td>10</td><td><a href="http://snomed.info/id/281867008">281867008 |Multisystem disorder|</a></td></tr></tbody></table>

***
