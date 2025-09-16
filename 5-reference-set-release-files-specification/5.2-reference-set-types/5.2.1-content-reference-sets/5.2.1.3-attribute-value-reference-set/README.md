# Attribute Value Reference Set

## Purpose

An [900000000000480006 | Attribute value type reference set|](http://snomed.info/id/900000000000480006) allows a value from a specified range to be associated with a component. This type of reference set can be used for a range of purposes where there is a requirement to provide additional information about particular concepts, descriptions or relationships. For example, an <mark style="color:blue;">|</mark>Attribute value type reference set<mark style="color:blue;">|</mark> is used to indicate the reason why a concept has been inactivated.

## Data Structure

An Attribute value reference set is a component reference set used to apply a tagged value to a SNOMED CT component. Its structure is shown in the following table.

**Attribute Value Reference Set - Data Structure**

<table data-full-width="true"><thead><tr><th width="208.56640625">Field</th><th width="99.15234375">Data type</th><th width="608.6609497070312">Purpose</th><th width="89.484375">Mutable</th><th>PK*</th></tr></thead><tbody><tr><td>id</td><td>UUID</td><td>A 128 bit unsigned Integer, uniquely identifying this reference set member.Different versions of a <em>reference set member</em> share the same id but have different effectiveTime. This allows a <em>reference set member</em> to be modified or made inactive (i.e. removed from the active set) at a specified time.</td><td><mark style="color:$danger;"><strong>NO</strong></mark></td><td><mark style="color:$success;"><strong>YES</strong></mark><br>(Full/Snapshot)</td></tr><tr><td>effectiveTime</td><td>Time</td><td><p>The inclusive date or time at which this version of the identified reference set member became the current version.</p><p><strong>Note</strong> : In distribution files the effectiveTime should follow the short ISO date format (<em>YYYYMM DD</em>) and should not include the hours, minutes, seconds or timezone indicator.The current version of this reference set member at time <em>T</em> is the version with the most recent effectiveTime prior to or equal to time <em>T</em>.</p></td><td><mark style="color:$success;"><strong>YES</strong></mark></td><td><mark style="color:$success;"><strong>YES</strong></mark> <br>(Full)<br><mark style="color:$success;">Optional</mark> (Snapshot)</td></tr><tr><td>active</td><td>Boolean</td><td>The state of the identified reference set member as at the specified effectiveTime. If active = 1 (true) the reference set member is part of the current version of the set, if active = 0 (false) the reference set member is not part of the current version of the set.</td><td><mark style="color:$success;"><strong>YES</strong></mark></td><td><mark style="color:$danger;"><strong>NO</strong></mark></td></tr><tr><td>moduleId</td><td>SCTID</td><td><p>Identifies the SNOMED CT module that contains this reference set member as at the specified effectiveTime .</p><p>The value must be a subtype of <a href="http://snomed.info/id/900000000000443000">900000000000443000 |Module (core metadata concept)|</a> within the metadata hierarchy.</p></td><td><mark style="color:$success;"><strong>YES</strong></mark></td><td><mark style="color:$danger;"><strong>NO</strong></mark></td></tr><tr><td>refsetId</td><td>SCTID</td><td><p>Identifies the reference set to which this reference set member belongs.</p><p>In this case, a subtype descendant of: <a href="http://snomed.info/id/900000000000480006">900000000000480006 |Attribute value type reference set|</a></p></td><td><mark style="color:$danger;"><strong>NO</strong></mark></td><td><mark style="color:$danger;"><strong>NO</strong></mark></td></tr><tr><td>referencedComponentId</td><td>SCTID</td><td>A reference to the SNOMED CT component to be included in the reference set.</td><td><mark style="color:$danger;"><strong>NO</strong></mark></td><td><mark style="color:$danger;"><strong>NO</strong></mark></td></tr><tr><td>valueId</td><td>SCTID</td><td>The tagged value applied to the referencedComponentId. A subtype of <a href="http://snomed.info/id/900000000000491004">900000000000491004 | Attribute value|</a> .</td><td><mark style="color:$success;"><strong>YES</strong></mark></td><td><mark style="color:$danger;"><strong>NO</strong></mark></td></tr></tbody></table>

***

{% hint style="info" %}
PK\* indicates if the attribute is part of the primary key for that file/table.
{% endhint %}

## Metadata

The metadata concepts shown below are examples of concepts that identify attribute value reference sets.

**Attribute Value Reference Sets in the Metadata Hierarchy**

> &#x20;[900000000000454005 |Foundation metadata concept|](http://snomed.info/id/900000000000454005)\
> &#x20;     [900000000000455006 |Reference set|](http://snomed.info/id/900000000000455006)\
> &#x20;            [900000000000480006 |Attribute value type|](http://snomed.info/id/900000000000480006)\
> &#x20;                 [900000000000489007 |Concept inactivation indicator reference set|](http://snomed.info/id/900000000000489007)\
> &#x20;                 [900000000000490003 |Description inactivation indicator reference set|](http://snomed.info/id/900000000000490003)\
> &#x20;                 [900000000000547002 |Relationship inactivation indicator reference set|](http://snomed.info/id/900000000000547002)  <sup><sub><mark style="color:$success;">< Not currently used<mark style="color:$success;"><sub></sup>&#x20;

{% hint style="info" %}
Note. Other attribute value reference sets exist but are not used to track component inactivation
{% endhint %}

***

**Concept Inactivation Values (with usage notes referring to the International Release)**

> &#x20;[900000000001043018 |Concept inactivation value|](http://snomed.info/id/900000000001043018)      \
> &#x20;        [723277005 |Nonconformance to editorial policy component|](http://snomed.info/id/723277005)   <sup><sub><mark style="color:$success;">< New introduced 2017-07-31<mark style="color:$success;"><sub></sup> \
> &#x20;        [900000000000482003 |Duplicate|](http://snomed.info/id/900000000000482003)\
> &#x20;        [900000000000483008 |Outdated|](http://snomed.info/id/900000000000483008)\
> &#x20;        [900000000000484002 |Ambiguous|](http://snomed.info/id/900000000000484002)\
> &#x20;        [900000000000485001 |Erroneous|](http://snomed.info/id/900000000000485001)\
> &#x20;        [900000000000486000 |Limited|](http://snomed.info/id/900000000000486000)\
> &#x20;        [900000000000487009 |Moved elsewhere|](http://snomed.info/id/900000000000487009)\
> &#x20;        [900000000000492006 |Pending move|](http://snomed.info/id/900000000000492006)   <sup><sub><mark style="color:$success;">< NEVER used for descriptions in the International Release - may have been used in extensions<mark style="color:$success;"><sub></sup>&#x20;

***

**Description Inactivation Values (with usage notes referring to the International Release)**

> [900000000001077011 |Description inactivation value|](http://snomed.info/id/900000000001077011)\
> &#x20;        [723277005 |Nonconformance to editorial policy component|](http://snomed.info/id/723277005)   <sup><sub><mark style="color:$success;">< New introduced 2017-07-31<mark style="color:$success;"><sub></sup> \
> &#x20;        [723278000 |Not semantically equivalent component|](http://snomed.info/id/723278000)    <sup><sub><mark style="color:$success;">< New introduced 2017-07-31<mark style="color:$success;"><sub></sup> \
> &#x20;        [900000000000483008 |Outdated|](http://snomed.info/id/900000000000483008)\
> &#x20;        [900000000000485001 |Erroneous|](http://snomed.info/id/900000000000485001)\
> &#x20;        [900000000000495008 |Concept non-current|](http://snomed.info/id/900000000000495008)\
> &#x20;        [900000000000486000 |Limited|](http://snomed.info/id/900000000000486000)    <sup><sub><mark style="color:$success;">< NOT used for description inactivations after 2010-07-31<mark style="color:$success;"><sub></sup>\
> &#x20;        [900000000000487009 |Moved elsewhere|](http://snomed.info/id/900000000000487009)    <sup><sub><mark style="color:$success;"><<mark style="color:$success;"><sub></sup> <sup><sub><mark style="color:$success;">NOT used for description inactivations before 2016-07-31 or after 2017-07-31<mark style="color:$success;"><sub></sup>\
> &#x20;        [900000000000482003 |Duplicate|](http://snomed.info/id/900000000000482003)        <sup><sub><mark style="color:$success;"><<mark style="color:$success;"><sub></sup> <sup><sub><mark style="color:$success;">NOT used for description inactivations before 2016-07-31 or after 2017-07-31<mark style="color:$success;"><sub></sup>\
> &#x20;        [900000000000494007 |Inappropriate|](http://snomed.info/id/900000000000494007)   <sup><sub><mark style="color:$success;">< NOT used for description inactivations before 2008-07-31 or after 2017-07-31<mark style="color:$success;"><sub></sup> \
> &#x20;        [900000000000492006 |Pending move|](http://snomed.info/id/900000000000492006)   <sup><sub><mark style="color:$success;">< NEVER used for descriptions in the International Release - may have been used in extensions<mark style="color:$success;"><sub></sup>&#x20;

***

## Reference Set Descriptor and Example Data

{% hint style="info" %}
**Notes on the tables used to show descriptors and examples**

The reference set example tables on this page have been revised as follows to aid clarity and understanding:

* The first four columns which are present in all release files are not shown. The omitted columns (id, effectiveTime, active, moduleId) are used in the same way in all referenced sets to support identification, versioning and packaging. They do not directly affect the specific features of a particular reference set or reference set type.
* Reference set columns that contain SNOMED CT identifiers are expanded to show details of the concept or description referenced by that identifier. In some cases, the term is shown in the same column using the expression syntax, in other cases an additional column with a name suffix '\_term' has been added. In the standard reference set files only the identifier is present in the column and there is no added column for the term. When using reference sets, the term and other details of the component are looked up from the relevant component release files.
{% endhint %}

#### Descriptor Template

The tables below show the descriptors that define examples of reference sets that follow the [|Attribute value type reference set|](http://snomed.info/id/900000000000480006) pattern.

**Refset Descriptor Rows for the Concept Inactivation Indicator Reference Set**

<table data-full-width="true"><thead><tr><th width="227.73748779296875">refsetId</th><th width="295.4312744140625">referencedComponentId  (Referenced component)</th><th width="244.87188720703125">attributeDescription  (Attribute description)</th><th width="220.231201171875">attributeType (Attribute type)</th><th>attributeOrder (Attribute order)</th></tr></thead><tbody><tr><td><a href="http://snomed.info/id/900000000000456007">900000000000456007 |Reference set descriptor|</a></td><td><a href="http://snomed.info/id/900000000000489007">900000000000489007 |Concept inactivation indicator reference set|</a></td><td><a href="http://snomed.info/id/449608002">449608002 |Referenced component|</a></td><td><a href="http://snomed.info/id/900000000000461009">900000000000461009 |Concept type component|</a></td><td>0</td></tr><tr><td><a href="http://snomed.info/id/900000000000456007">900000000000456007 |Reference set descriptor|</a></td><td><a href="http://snomed.info/id/900000000000489007">900000000000489007 |Concept inactivation indicator reference set|</a></td><td><a href="http://snomed.info/id/900000000000481005">900000000000481005 |Concept inactivation value|</a></td><td><a href="http://snomed.info/id/900000000000461009">900000000000461009 |Concept type component|</a></td><td>1</td></tr></tbody></table>

***

**Refset Descriptor Rows for the Description Inactivation Indicator Reference Set**

<table data-full-width="true"><thead><tr><th width="224.24456787109375">refsetId</th><th width="320.79144287109375">referencedComponentId (Referenced component)</th><th width="253.3765869140625">attributeDescription (Attribute description)</th><th width="247.4561767578125">attributeType (Attribute type)</th><th>attributeOrder (Attribute order)</th></tr></thead><tbody><tr><td><a href="http://snomed.info/id/900000000000456007">900000000000456007 |Reference set descriptor|</a></td><td><p></p><p><a href="http://snomed.info/id/900000000000490003">900000000000490003 |Description inactivation indicator reference set|</a><br><br></p></td><td><a href="http://snomed.info/id/449608002">449608002 |Referenced component|</a></td><td><a href="http://snomed.info/id/900000000000462002">900000000000462002 |Description type component|</a></td><td>0</td></tr><tr><td><a href="http://snomed.info/id/900000000000456007">900000000000456007 |Reference set descriptor|</a></td><td><p></p><p><a href="http://snomed.info/id/900000000000490003">900000000000490003 |Description inactivation indicator reference set|</a></p></td><td><a href="http://snomed.info/id/900000000000493001">900000000000493001 |Description inactivation value|</a></td><td><a href="http://snomed.info/id/900000000000461009">900000000000461009 |Concept type component|</a></td><td>1</td></tr></tbody></table>

***

**Sample Rows from the Concept Inactivation Indicator Reference Set**

<table><thead><tr><th width="298.62811279296875">refsetId</th><th width="337.0321044921875">referencedComponentId (Referenced component)</th><th width="240.637451171875">valueId (Concept inactivation value)</th></tr></thead><tbody><tr><td><a href="http://snomed.info/id/900000000000489007">900000000000489007 |Concept inactivation indicator reference set|</a></td><td><a href="http://snomed.info/id/105000">105000 |Poisoning by pharmaceutical excipient|</a></td><td><a href="http://snomed.info/id/900000000000482003">900000000000482003 |Duplicate|</a></td></tr><tr><td><a href="http://snomed.info/id/900000000000489007">900000000000489007 |Concept inactivation indicator reference set|</a></td><td><a href="http://snomed.info/id/123008">123008 |Channel catfish virus disease|</a></td><td><a href="http://snomed.info/id/900000000000487009">900000000000487009 |Moved elsewhere|</a></td></tr><tr><td><a href="http://snomed.info/id/900000000000489007">900000000000489007 |Concept inactivation indicator reference set|</a></td><td><a href="http://snomed.info/id/141000">141000 |Glaucoma as birth trauma|</a></td><td><a href="http://snomed.info/id/900000000000482003">900000000000482003 |Duplicate|</a></td></tr><tr><td><a href="http://snomed.info/id/900000000000489007">900000000000489007 |Concept inactivation indicator reference set|</a></td><td><a href="http://snomed.info/id/157000">157000 |AIDS with low vision|</a></td><td><a href="http://snomed.info/id/900000000000484002">900000000000484002 |Ambiguous|</a></td></tr><tr><td><a href="http://snomed.info/id/900000000000489007">900000000000489007 |Concept inactivation indicator reference set|</a></td><td><a href="http://snomed.info/id/190000">190000 |Partial hysterectomy|</a></td><td><a href="http://snomed.info/id/900000000000484002">900000000000484002 |Ambiguous|</a></td></tr><tr><td><a href="http://snomed.info/id/900000000000489007">900000000000489007 |Concept inactivation indicator reference set|</a></td><td><a href="http://snomed.info/id/203004">203004 |Replacement of pacemaker in brain|</a></td><td><a href="http://snomed.info/id/900000000000484002">900000000000484002 |Ambiguous|</a></td></tr><tr><td><a href="http://snomed.info/id/900000000000489007">900000000000489007 |Concept inactivation indicator reference set|</a></td><td><a href="http://snomed.info/id/212002">212002 |Salmonella III arizonae 53:k:z|</a></td><td><a href="http://snomed.info/id/900000000000483008">900000000000483008 |Outdated|</a></td></tr><tr><td><a href="http://snomed.info/id/900000000000489007">900000000000489007 |Concept inactivation indicator reference set|</a></td><td><a href="http://snomed.info/id/215000">215000 |Operative procedure on fingers|</a></td><td><a href="http://snomed.info/id/900000000000482003">900000000000482003 |Duplicate|</a></td></tr><tr><td><a href="http://snomed.info/id/900000000000489007">900000000000489007 |Concept inactivation indicator reference set|</a></td><td><a href="http://snomed.info/id/220000">220000 |Unspecified monoarthritis|</a></td><td><a href="http://snomed.info/id/900000000000486000">900000000000486000 |Limited|</a></td></tr><tr><td><a href="http://snomed.info/id/900000000000489007">900000000000489007 |Concept inactivation indicator reference set|</a></td><td><a href="http://snomed.info/id/236003">236003 |Incision of vein|</a></td><td><a href="http://snomed.info/id/900000000000484002">900000000000484002 |Ambiguous|</a></td></tr></tbody></table>

***






<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&entry.1767247133=Release+File+Specification&entry.670899847=Attribute%20Value%20Reference%20Set" class="button primary">Provide Feedback</a>
