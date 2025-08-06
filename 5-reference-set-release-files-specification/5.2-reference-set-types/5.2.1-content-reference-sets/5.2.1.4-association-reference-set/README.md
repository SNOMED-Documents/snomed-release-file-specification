# Association Reference Set

## Purpose

An [900000000000521006 |Association type reference set|](http://snomed.info/id/900000000000521006) represents a set of unordered associations of a particular type between components.

## Data structure

An Association reference set is a reference set used to represent associations between components. Its structure is shown in the following table.

Table 5.2.1.4-1: Association Reference Set - Data Structure

<table data-header-hidden data-full-width="true"><thead><tr><th width="208.56640625"></th><th width="99.15234375"></th><th width="303.1640625"></th><th width="89.484375"></th><th></th></tr></thead><tbody><tr><td><strong>Field</strong></td><td><strong>Data type</strong></td><td><strong>Purpose</strong></td><td><strong>Mutable</strong></td><td><strong>Part of Primary Key</strong></td></tr><tr><td>id</td><td>UUID</td><td>A 128 bit unsigned Integer, uniquely identifying this reference set member.Different versions of a <em>reference set member</em> share the same id but have different effectiveTime. This allows a <em>reference set member</em> to be modified or made inactive (i.e. removed from the active set) at a specified time.</td><td><mark style="color:$danger;">NO</mark></td><td><mark style="color:$success;">YES</mark><br>(Full/Snapshot)</td></tr><tr><td>effectiveTime</td><td>Time</td><td><p>The inclusive date or time at which this version of the identified reference set member became the current version.</p><p><strong>Note</strong> : In distribution files the effectiveTime should follow the short ISO date format (<em>YYYYMM DD</em>) and should not include the hours, minutes, seconds or timezone indicator.The current version of this reference set member at time <em>T</em> is the version with the most recent effectiveTime prior to or equal to time <em>T</em>.</p></td><td><mark style="color:$success;">YES</mark></td><td><mark style="color:$success;">YES</mark> <br>(Full)<br><mark style="color:$success;">Optional</mark> (Snapshot)</td></tr><tr><td>active</td><td>Boolean</td><td>The state of the identified reference set member as at the specified effectiveTime. If active = 1 (true) the reference set member is part of the current version of the set, if active = 0 (false) the reference set member is not part of the current version of the set.</td><td><mark style="color:$success;">YES</mark></td><td><mark style="color:$danger;">NO</mark></td></tr><tr><td>moduleId</td><td>SCTID</td><td><p>Identifies the SNOMED CT module that contains this reference set member as at the specified effectiveTime .</p><p>The value must be a subtype of <a href="http://snomed.info/id/900000000000443000">900000000000443000 |Module (core metadata concept)|</a> within the metadata hierarchy.</p></td><td><mark style="color:$success;">YES</mark></td><td><mark style="color:$danger;">NO</mark></td></tr><tr><td>refsetId</td><td>SCTID</td><td><p>Identifies the reference set to which this reference set member belongs.</p><p>A subtype descendant of:</p><p><a href="http://snomed.info/id/446609009">4</a><a href="http://snomed.info/id/900000000000521006">900000000000521006 |Association type|</a></p></td><td><mark style="color:$danger;">NO</mark></td><td><mark style="color:$danger;">NO</mark></td></tr><tr><td>referencedComponentId</td><td>SCTID</td><td>A reference to the SNOMED CT component to be included in the reference set.</td><td><mark style="color:$danger;">NO</mark></td><td><mark style="color:$danger;">NO</mark></td></tr><tr><td>targetComponentId</td><td>SCTID</td><td>The identifier of the target component of the association.<br>Note. An inconsistency in this specification was resolved by the Modeling Advisory Group 2018-10-15 decision that this field should be mutable.</td><td><mark style="color:$success;">YES</mark></td><td><mark style="color:$danger;">NO</mark></td></tr></tbody></table>

## Metadata

The following metadata supports this reference set:

Table 5.2.1.4-2: Association Reference Sets in the Metadata Hierarchy

<table data-header-hidden data-full-width="true"><thead><tr><th></th></tr></thead><tbody><tr><td> <a href="http://snomed.info/id/900000000000455006">900000000000455006 |Reference set|</a><br>         <a href="http://snomed.info/id/900000000000521006">900000000000521006 |Association type|</a><br>                 <a href="http://snomed.info/id/734138000">734138000 |Anatomy structure and entire association reference set|</a><br>                 <a href="http://snomed.info/id/734139008">734139008 |Anatomy structure and part association reference set|</a><br>                 <a href="http://snomed.info/id/900000000000522004">900000000000522004 |Historical association|</a> <mark style="color:$success;">- this has many subtypes</mark></td></tr></tbody></table>

\


## Example Descriptors and Data

See [5.2.5.1 Historical Association Reference Sets](../../../../5%20reference-set-release-files-specification/5.2%20reference-set-types/5.2.1%20content-reference-sets/5.2.5.1-Historical-Association-Reference-Sets_106693955.html) for an example of the reference set description and data representation in an association type reference set.
