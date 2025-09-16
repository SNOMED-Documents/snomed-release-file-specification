# Association Reference Set

## Purpose

An [900000000000521006 |Association type reference set|](http://snomed.info/id/900000000000521006) represents a set of unordered associations of a particular type between components.

## Data structure

An Association reference set is a reference set used to represent associations between components. Its structure is shown in the following table.

**Association Reference Set - Data Structure**

<table data-full-width="true"><thead><tr><th width="208.56640625">Field</th><th width="99.15234375">Data type</th><th width="600.5796508789062">Purpose</th><th width="89.484375">Mutable</th><th>PK*</th></tr></thead><tbody><tr><td>id</td><td>UUID</td><td>A 128 bit unsigned Integer, uniquely identifying this reference set member.Different versions of a <em>reference set member</em> share the same id but have different effectiveTime. This allows a <em>reference set member</em> to be modified or made inactive (i.e. removed from the active set) at a specified time.</td><td><mark style="color:$danger;"><strong>NO</strong></mark></td><td><mark style="color:$success;"><strong>YES</strong></mark><br>(Full/Snapshot)</td></tr><tr><td>effectiveTime</td><td>Time</td><td><p>The inclusive date or time at which this version of the identified reference set member became the current version.</p><p><strong>Note</strong> : In distribution files the effectiveTime should follow the short ISO date format (<em>YYYYMM DD</em>) and should not include the hours, minutes, seconds or timezone indicator.The current version of this reference set member at time <em>T</em> is the version with the most recent effectiveTime prior to or equal to time <em>T</em>.</p></td><td><mark style="color:$success;"><strong>YES</strong></mark></td><td><mark style="color:$success;"><strong>YES</strong></mark> <br>(Full)<br><mark style="color:$success;">Optional</mark> (Snapshot)</td></tr><tr><td>active</td><td>Boolean</td><td>The state of the identified reference set member as at the specified effectiveTime. If active = 1 (true) the reference set member is part of the current version of the set, if active = 0 (false) the reference set member is not part of the current version of the set.</td><td><mark style="color:$success;"><strong>YES</strong></mark></td><td><mark style="color:$danger;"><strong>NO</strong></mark></td></tr><tr><td>moduleId</td><td>SCTID</td><td><p>Identifies the SNOMED CT module that contains this reference set member as at the specified effectiveTime .</p><p>The value must be a subtype of <a href="http://snomed.info/id/900000000000443000">900000000000443000 |Module (core metadata concept)|</a> within the metadata hierarchy.</p></td><td><mark style="color:$success;"><strong>YES</strong></mark></td><td><mark style="color:$danger;"><strong>NO</strong></mark></td></tr><tr><td>refsetId</td><td>SCTID</td><td><p>Identifies the reference set to which this reference set member belongs.</p><p>In this case, a subtype descendant of: <a href="http://snomed.info/id/900000000000521006">900000000000521006 |Association type|</a>.</p></td><td><mark style="color:$danger;"><strong>NO</strong></mark></td><td><mark style="color:$danger;"><strong>NO</strong></mark></td></tr><tr><td>referencedComponentId</td><td>SCTID</td><td>A reference to the SNOMED CT component to be included in the reference set. The source component of the association.</td><td><mark style="color:$danger;"><strong>NO</strong></mark></td><td><mark style="color:$danger;"><strong>NO</strong></mark></td></tr><tr><td>targetComponentId</td><td>SCTID</td><td>The identifier of the target component of the association.<br>Note. An inconsistency in this specification was resolved by the Modeling Advisory Group 2018-10-15 decision that this field should be mutable.</td><td><mark style="color:$success;"><strong>YES</strong></mark></td><td><mark style="color:$danger;"><strong>NO</strong></mark></td></tr></tbody></table>

***

{% hint style="info" %}
PK\* indicates if the attribute is part of the primary key for that file/table.
{% endhint %}

## Metadata

The following metadata supports this reference set:

**Association Reference Sets in the Metadata Hierarchy**

> &#x20;[900000000000455006 |Reference set|](http://snomed.info/id/900000000000455006)\
> &#x20;        [900000000000521006 |Association type|](http://snomed.info/id/900000000000521006)\
> &#x20;                [734138000 |Anatomy structure and entire association reference set|](http://snomed.info/id/734138000)\
> &#x20;                [734139008 |Anatomy structure and part association reference set|](http://snomed.info/id/734139008)\
> &#x20;                [900000000000522004 |Historical association|](http://snomed.info/id/900000000000522004) <mark style="color:$success;">- this has many subtypes</mark>

***

## Example Descriptors and Data

See [Historical Association Reference Sets](5.2.5.1-historical-association-reference-sets.md) for an example of the reference set description and data representation in an association type reference set.






<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&entry.1767247133=Release+File+Specification&entry.670899847=Association%20Reference%20Set" class="button primary">Provide Feedback</a>
