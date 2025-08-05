# Attribute Value Reference Set

## Purpose

An [900000000000480006 | Attribute value type reference set|](http://snomed.info/id/900000000000480006) allows a value from a specified range to be associated with a component. This type of reference set can be used for a range of purposes where there is a requirement to provide additional information about particular concepts, descriptions or relationships. For example, an <mark style="color:blue;">|</mark>Attribute value type reference set<mark style="color:blue;">|</mark> is used to indicate the reason why a concept has been inactivated.

## Data Structure

An Attribute value reference set is a component reference set used to apply a tagged value to a SNOMED CT component. Its structure is shown in the following table.

Table 5.2.1.3-1: Attribute Value Reference Set - Data Structure

<table data-header-hidden data-full-width="true"><thead><tr><th width="208.56640625"></th><th width="99.15234375"></th><th width="303.1640625"></th><th width="89.484375"></th><th></th></tr></thead><tbody><tr><td><strong>Field</strong></td><td><strong>Data type</strong></td><td><strong>Purpose</strong></td><td><strong>Mutable</strong></td><td><strong>Part of Primary Key</strong></td></tr><tr><td>id</td><td>UUID</td><td>A 128 bit unsigned Integer, uniquely identifying this reference set member.Different versions of a <em>reference set member</em> share the same id but have different effectiveTime. This allows a <em>reference set member</em> to be modified or made inactive (i.e. removed from the active set) at a specified time.</td><td><mark style="color:$danger;">NO</mark></td><td><mark style="color:$success;">YES</mark><br>(Full/Snapshot)</td></tr><tr><td>effectiveTime</td><td>Time</td><td><p>The inclusive date or time at which this version of the identified reference set member became the current version.</p><p><strong>Note</strong> : In distribution files the effectiveTime should follow the short ISO date format (<em>YYYYMM DD</em>) and should not include the hours, minutes, seconds or timezone indicator.The current version of this reference set member at time <em>T</em> is the version with the most recent effectiveTime prior to or equal to time <em>T</em>.</p></td><td><mark style="color:$success;">YES</mark></td><td><mark style="color:$success;">YES</mark> <br>(Full)<br><mark style="color:$success;">Optional</mark> (Snapshot)</td></tr><tr><td>active</td><td>Boolean</td><td>The state of the identified reference set member as at the specified effectiveTime. If active = 1 (true) the reference set member is part of the current version of the set, if active = 0 (false) the reference set member is not part of the current version of the set.</td><td><mark style="color:$success;">YES</mark></td><td><mark style="color:$danger;">NO</mark></td></tr><tr><td>moduleId</td><td>SCTID</td><td><p>Identifies the SNOMED CT module that contains this reference set member as at the specified effectiveTime .</p><p>The value must be a subtype of <a href="http://snomed.info/id/900000000000443000">900000000000443000 |Module (core metadata concept)|</a> within the metadata hierarchy.</p></td><td><mark style="color:$success;">YES</mark></td><td><mark style="color:$danger;">NO</mark></td></tr><tr><td>refsetId</td><td>SCTID</td><td><p>Identifies the reference set to which this reference set member belongs.</p><p>In this case, a subtype descendant of: <a href="http://snomed.info/id/900000000000480006">900000000000480006 |Attribute value type reference set|</a></p></td><td><mark style="color:$danger;">NO</mark></td><td><mark style="color:$danger;">NO</mark></td></tr><tr><td>referencedComponentId</td><td>SCTID</td><td>A reference to the SNOMED CT component to be included in the reference set.</td><td><mark style="color:$danger;">NO</mark></td><td><mark style="color:$danger;">NO</mark></td></tr><tr><td>valueId</td><td>SCTID</td><td>The tagged value applied to the referencedComponentId. A subtype of <a href="http://snomed.info/id/900000000000491004">900000000000491004 | Attribute value|</a> .</td><td><mark style="color:$success;">YES</mark></td><td><mark style="color:$danger;">NO</mark></td></tr></tbody></table>

## Metadata

The metadata concepts shown in Table 5.2.1.3-2 are examples of concepts that identify attribute value reference sets.

Table 5.2.1.3-2: Attribute Value Reference Sets in the Metadata Hierarchy

<table data-header-hidden data-full-width="true"><thead><tr><th></th></tr></thead><tbody><tr><td> <a href="http://snomed.info/id/900000000000454005">900000000000454005 |Foundation metadata concept|</a><br>      <a href="http://snomed.info/id/900000000000455006">900000000000455006 |Reference set|</a><br>             <a href="http://snomed.info/id/900000000000480006">900000000000480006 |Attribute value type|</a><br>                  <a href="http://snomed.info/id/900000000000489007">900000000000489007 |Concept inactivation indicator reference set|</a><br>                  <a href="http://snomed.info/id/900000000000490003">900000000000490003 |Description inactivation indicator reference set|</a><br>                  <a href="http://snomed.info/id/900000000000547002">900000000000547002 |Relationship inactivation indicator reference set|</a>  <mark style="color:$success;">&#x3C; Not currently used</mark> <br>  <mark style="color:$success;">Note. Other attribute value reference sets exist but are not used to track component inactivation</mark></td></tr></tbody></table>

Item 5.2.1.3-1: Concept Inactivation Values (with usage notes)

<table data-header-hidden data-full-width="true"><thead><tr><th></th></tr></thead><tbody><tr><td><p> <a href="http://snomed.info/id/900000000001043018">900000000001043018 |Concept inactivation value|</a>      <br>         <a href="http://snomed.info/id/723277005">723277005 |Nonconformance to editorial policy component|</a>   <mark style="color:$success;">&#x3C; New introduced 2017-07-31</mark> <br>         <a href="http://snomed.info/id/900000000000482003">900000000000482003 |Duplicate|</a><br>         <a href="http://snomed.info/id/900000000000483008">900000000000483008 |Outdated|</a><br>         <a href="http://snomed.info/id/900000000000484002">900000000000484002 |Ambiguous|</a><br>         <a href="http://snomed.info/id/900000000000485001">900000000000485001 |Erroneous|</a><br>         <a href="http://snomed.info/id/900000000000486000">900000000000486000 |Limited|</a><br>         <a href="http://snomed.info/id/900000000000487009">900000000000487009 |Moved elsewhere|</a><br>         <a href="http://snomed.info/id/900000000000492006">900000000000492006 |Pending move|</a>   <mark style="color:$success;">&#x3C; NEVER used for descriptions in the International</mark>                            </p><p>                                                                                            <mark style="color:$success;">Release - may have been used in extensions</mark> </p></td></tr></tbody></table>



Table 5.2.1.3-3: Description Inactivation Values (with usage notes)

900000000001077011 [900000000001077011 |Description inactivation value|](http://snomed.info/id/900000000001077011)\
[723277005 |Nonconformance to editorial policy component|](http://snomed.info/id/723277005) /\* <-- New value introduced in 2017-07-31 International Release _/_\
[_723278000 |Not semantically equivalent component|_](http://snomed.info/id/723278000) _/_ <-- New value introduced in 2017-07-31 International Release _/_\
[_900000000000483008 |Outdated|_](http://snomed.info/id/900000000000483008)\
[_900000000000485001 |Erroneous|_](http://snomed.info/id/900000000000485001)\
[_900000000000495008 |Concept non-current|_](http://snomed.info/id/900000000000495008)\
[_900000000000486000 |Limited|_](http://snomed.info/id/900000000000486000) _/_ <-- NOT used for description inactivations after 2010-07-31 International Releases _/_\
[_900000000000487009 |Moved elsewhere|_](http://snomed.info/id/900000000000487009) _/_ <-- NOT used for description inactivations before 2016-07-31 or after 2017-07-31 International Releases _/_\
[_900000000000482003 |Duplicate|_](http://snomed.info/id/900000000000482003) _/_ <-- NOT used for description inactivations before 2016-07-31 or after 2017-07-31 International Releases _/_\
[_900000000000494007 |Inappropriate|_](http://snomed.info/id/900000000000494007) _/_ <-- NOT used for description inactivations before 2008-07-31 or after 2017-07-31 International Releases _/_\
[_900000000000492006 |Pending move|_](http://snomed.info/id/900000000000492006) _/_ <-- NEVER used for descriptions in the International Release - may have been used in extensions \*/

## Reference Set Descriptor and Example Data

### Descriptor Template

The tables below show the descriptors that define examples of [reference sets](https://confluence.ihtsdotools.org/display/DOCGLOSS/reference+set) that follow the [900000000000480006 | Attribute value type reference set|](http://snomed.info/id/900000000000480006) pattern.

Table 5.2.1.3-4: Refset Descriptor Rows for the Concept Inactivation Indicator Reference Set

| **refsetId**          | **referencedComponentId (Referenced component)** | **attributeDescription (Attribute description)**                | **attributeType (Attribute type)** | **attributeOrder (Attribute order)** |
| --------------------- | ------------------------------------------------ | --------------------------------------------------------------- | ---------------------------------- | ------------------------------------ |
| \[ 900000000000456007 | Reference set descriptor                         | ]\(http://snomed.info/id/900000000000456007 "900000000000456007 | Reference set descriptor           | ")                                   |
| \[ 900000000000456007 | Reference set descriptor                         | ]\(http://snomed.info/id/900000000000456007 "900000000000456007 | Reference set descriptor           | ")                                   |

Table 5.2.1.3-5: Refset Descriptor Rows for the Description Inactivation Indicator Reference Set

| **refsetId**          | **referencedComponentId (Referenced component)** | **attributeDescription (Attribute description)**                | **attributeType (Attribute type)** | **attributeOrder (Attribute order)** |
| --------------------- | ------------------------------------------------ | --------------------------------------------------------------- | ---------------------------------- | ------------------------------------ |
| \[ 900000000000456007 | Reference set descriptor                         | ]\(http://snomed.info/id/900000000000456007 "900000000000456007 | Reference set descriptor           | ")                                   |
| \[ 900000000000456007 | Reference set descriptor                         | ]\(http://snomed.info/id/900000000000456007 "900000000000456007 | Reference set descriptor           | ")                                   |

### Example Data

Example 5.2.1.3-1: Sample Rows from the Concept Inactivation Indicator Reference Set

| **refsetId**          | **referencedComponentId (Referenced component)** | **valueId (Concept inactivation value)**                        |
| --------------------- | ------------------------------------------------ | --------------------------------------------------------------- |
| \[ 900000000000489007 | Concept inactivation indicator reference set     | ]\(http://snomed.info/id/900000000000489007 "900000000000489007 |
| \[ 900000000000489007 | Concept inactivation indicator reference set     | ]\(http://snomed.info/id/900000000000489007 "900000000000489007 |
| \[ 900000000000489007 | Concept inactivation indicator reference set     | ]\(http://snomed.info/id/900000000000489007 "900000000000489007 |
| \[ 900000000000489007 | Concept inactivation indicator reference set     | ]\(http://snomed.info/id/900000000000489007 "900000000000489007 |
| \[ 900000000000489007 | Concept inactivation indicator reference set     | ]\(http://snomed.info/id/900000000000489007 "900000000000489007 |
| \[ 900000000000489007 | Concept inactivation indicator reference set     | ]\(http://snomed.info/id/900000000000489007 "900000000000489007 |
| \[ 900000000000489007 | Concept inactivation indicator reference set     | ]\(http://snomed.info/id/900000000000489007 "900000000000489007 |
| \[ 900000000000489007 | Concept inactivation indicator reference set     | ]\(http://snomed.info/id/900000000000489007 "900000000000489007 |
| \[ 900000000000489007 | Concept inactivation indicator reference set     | ]\(http://snomed.info/id/900000000000489007 "900000000000489007 |
| \[ 900000000000489007 | Concept inactivation indicator reference set     | ]\(http://snomed.info/id/900000000000489007 "900000000000489007 |
| \[code]               |                                                  |                                                                 |

\[/code]
