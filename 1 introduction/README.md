# Introduction

## Background

SNOMED CT is the most comprehensive and precise clinical health terminology product in the world. It has been developed collaboratively to ensure it meets the diverse needs and expectations of clinicians worldwide and is accepted as a common global language for health terms. SNOMED CT enables meaning-based retrieval and processing of clinical data because it applies description logic techniques to represent the meaning of clinical concepts. As a result, patients and healthcare professionals benefit from improved health records, clinical decisions and analysis, leading to higher quality, consistency and safety in healthcare delivery.

SNOMED International distributes SNOMED CT to its licensees as a package of release files that can be loaded into software applications that enable and optimize access to the terminology.

## Purpose

This document provides the formal specification of the file structures in which SNOMED CT is distributed. The specified file structures apply to the releases of the SNOMED CT International Edition, and to SNOMED CT extensions distributed by Members and Affiliates .

## Audience

The intended audiences for this guide are those involved in the creating or consuming SNOMED CT release files. This includes:

* SNOMED International staff involved in creating or quality assuring SNOMED CT release files.
* National Release Centers and Affiliates that create, maintain and distribute SNOMED CT extensions.
* Software designers and developers responsible for SNOMED CT enabled software applications that need to access data provided in SNOMED CT release files.
* Anyone interested in a detailed understanding of the logical design of SNOMED CT and way that logical design is represented in release files.

Notes

{% hint style="warning" %}
Licensing Note

This guide refers to files that are included in the International Release of SNOMED CT provided to licensees by SNOMED International. It also refers to additional files that are included in SNOMED CT extensions provided by Members and Affiliates..

Details of the licensing conditions for SNOMED CT are available from the SNOMED International web site (www.snomed.org)
{% endhint %}

{% hint style="warning" %}
Update Note

Starting on 31 July 2018, two new reference sets are being introduced to provide a more expressive representation of concept definitions. Initially these files will only contain supplementary information that cannot be represented in the current  stated relationship file. From 2019 onward, these new references sets will include the full representation of the  stated view of all concept definitions and on completion of the transitional process the stated relationship file will be deprecated.

Further details of this change are provided in the relevant sections of this specification. As this version to the guide is being published at the start of the transitional period, it includes specifications of current files and newly introduced files.
{% endhint %}

{% hint style="info" %}
Historical Note

This document specifies release file structures known as Release Format 2 (RF2). These file structures were introduced in January 2012 to support built-in version tracking and more flexible extensibility mechanisms, including reference sets and packaging of release files into separately identifiable modules. Between its initial release in January 2002 and January 2012, SNOMED CT release files were structured in accordance with an earlier file structure specifications that are now referred to a Release Format 1 (RF1). That release format is deprecated not longer used or supported by SNOMED International.
{% endhint %}
