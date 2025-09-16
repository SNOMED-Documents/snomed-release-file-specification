# Description File Specification

The Description holds descriptionsthat describe SNOMED CT concepts. A description is used to give meaning to a concept and provide well-understood and standard ways of referring to a concept.

***

**Description file - Detailed Specification**

<table data-full-width="true"><thead><tr><th width="128.4312744140625">Field</th><th width="84.74371337890625">Data type</th><th width="661.2766723632812">Purpose</th><th width="90.16796875">Mutable</th><th width="141.29296875">PK*</th></tr></thead><tbody><tr><td>id</td><td>SCTID</td><td>Uniquely identifies the description.</td><td><mark style="color:red;"><strong>NO</strong></mark></td><td><mark style="color:green;"><strong>YES</strong></mark><br>(Full/Snapshot)</td></tr><tr><td>effectiveTime</td><td>Time</td><td><p>Specifies the inclusive date at which the component version's state became the then current valid state of the component</p><p><strong>Note</strong> : In distribution files the effectiveTime should follow the short ISO date format (<em>YYYYMM DD</em>) and should not include the hours, minutes, seconds or timezone indicator.</p></td><td><mark style="color:green;"><strong>YES</strong></mark></td><td><p><mark style="color:green;"><strong>YES</strong></mark> </p><p>(Full)</p><p><mark style="color:green;">Optional</mark> (Snapshot)</p></td></tr><tr><td>active</td><td>Boolean</td><td>Specifies whether the state of the description was active or inactive from the nominal release date specified by the effectiveTime .</td><td><mark style="color:green;"><strong>YES</strong></mark></td><td><mark style="color:red;"><strong>NO</strong></mark></td></tr><tr><td>moduleId</td><td>SCTID</td><td>Identifies the description version's module. Set to a child of <a href="http://snomed.info/id/900000000000443000">900000000000443000 | Module|</a> within the metadata hierarchy.</td><td><mark style="color:green;"><strong>YES</strong></mark></td><td><mark style="color:red;"><strong>NO</strong></mark></td></tr><tr><td>conceptId</td><td>SCTID</td><td>Identifies the concept to which this description applies. Set to the identifier of a concept in the <mark style="color:blue;">|</mark>SNOMED CT Concept<mark style="color:blue;">|</mark> hierarchy within the Concept. Note that a specific version of a description is not directly bound to a specific version of the concept to which it applies. Which version of a description applies to a concept depends on its effectiveTime and the point in time at which it is accessed.</td><td><mark style="color:red;"><strong>NO</strong></mark></td><td><mark style="color:red;"><strong>NO</strong></mark></td></tr><tr><td>languageCode</td><td>String</td><td>Specifies the language of the description text using the two character ISO-639-1 code. Note that this specifies a language level only, not a dialect or country code.</td><td><mark style="color:red;"><strong>NO</strong></mark></td><td><mark style="color:red;"><strong>NO</strong></mark></td></tr><tr><td>typeId</td><td>SCTID</td><td>Identifies whether the description is fully specified name a synonym or other description type. This field is set to a child of <a href="http://snomed.info/id/900000000000446008">900000000000446008 | Description type|</a> in the Metadata hierarchy.</td><td><mark style="color:red;"><strong>NO</strong></mark></td><td><mark style="color:red;"><strong>NO</strong></mark></td></tr><tr><td>term</td><td>String</td><td>The description version's text value, represented in UTF-8 encoding</td><td><mark style="color:green;"><strong>YES</strong></mark></td><td><mark style="color:red;"><strong>NO</strong></mark></td></tr><tr><td>caseSignificanceId</td><td>SCTID</td><td>Identifies the concept enumeration value that represents the case significance of this description version. For example, the term may be completely case sensitive, case insensitive or initial letter case insensitive. This field will be set to a child of <a href="http://snomed.info/id/900000000000447004">900000000000447004 | Case significance|</a> within the metadata hierarchy.</td><td><mark style="color:green;"><strong>YES</strong></mark></td><td><mark style="color:red;"><strong>NO</strong></mark></td></tr></tbody></table>

{% hint style="info" %}
PK\* indicates if the attribute is part of the primary key for that file/table.
{% endhint %}

Only one description record with the same id field will be current at any point in time. The current record will be the one with the most recent effectiveTime before or equal to the point in time under consideration.

If the active field of this record is false ('0'), then the description is inactive at that point in time. If the activefield is true ('1'), then the description is associated with the concept identified by the conceptId field.

The conceptId field, the languageCode field and the typeId field will not change between two rows with the same id, in other words they are immutable. Where a change is required to one of these fields, then the component will be inactivated (by appending a row with the same id and the active field set to false) and a another row will be added representing a new component with a new id. Only limited changes may be made to the term field, as defined by editorial rules.

Each concept will have at least one active description with a typeId of <mark style="color:blue;">|</mark>synonym<mark style="color:blue;">|</mark> and at least one active description with a typeId of <mark style="color:blue;">|</mark>Fully specified name<mark style="color:blue;">|</mark>.

Where a concept only has one active description with a typeId of <mark style="color:blue;">|</mark>Fully specified name<mark style="color:blue;">|</mark> across all language codes within a release, then that Description can be taken as the Fully Specified Name for all languages and dialects, and need not be explicitly included in every language reference set associated with that release.

The term field will be restricted as follows:

* to an overall maximum length of 32Kb;
* to a maximum length, configurable for each description type as defined in the [900000000000538005 | Description format reference set|](http://snomed.info/id/900000000000538005) member associated with that description type- see the [Description Format Reference Set](<../../../5 reference-set-release-files-specification/5.2 reference-set-types/5.2.4 metadata-reference-sets/5.2.4.3-description-format-reference-set.md>) specifications document for more details.
* The Description Format Reference Set also defined the format of the term field (plain text, limited HTML, XHTML) for each description type.
* Control characters (including TABs, CRs and LFs) will not appear in [900000000000540000 | Plain text|](http://snomed.info/id/900000000000540000) or [900000000000541001 | Limited HTML|](http://snomed.info/id/900000000000541001) format types.

## Related Links

* [Description Format Reference Set](<../../../5 reference-set-release-files-specification/5.2 reference-set-types/5.2.4 metadata-reference-sets/5.2.4.3-description-format-reference-set.md>)
* [Appendix C. Unicode UTF-8 encoding](../../../appendices/appendix-c-unicode-utf-8-encoding.md)







<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&entry.1767247133=Release+File+Specification&entry.670899847=Description%20File%20Specification" class="button primary">Provide Feedback</a>
