# Stated Relationship file

{% hint style="danger" %}
The stated relationships file is no longer maintained and distributed. From July 2019 it was replaced by the [OWL Expression Reference Set file](../o/owl-expression-reference-set-file.md).
{% endhint %}

A previously used distribution file that contained the stated form represented by SNOMED CT relationships .

Notes:

1. The stated form of a Concept is the Description Logic definition that is directly edited by authors or editors. It consists of the stated [116680003 |is a|](http://snomed.info/id/116680003) relationships plus the defining relationships that exist prior to running a classifier on the logic definitions.
2. Prior to July 2019 the stated form of a Concept was represented by a collection of relationships: one or more <mark style="color:blue;">|</mark>Is a<mark style="color:blue;">|</mark> relationships and zero or more defining relationships .
3. The Stated Relationships File was in the same table format as the Relationships File, but the value of the characteristicTypeId field is [900000000000010007 |Stated relationship (core metadata concept)|](http://snomed.info/id/900000000000010007) .
