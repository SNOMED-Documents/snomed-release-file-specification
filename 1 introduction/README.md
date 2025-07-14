# 1. Introduction

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

{% hint style="info" %}
Historical Note

This document specifies release file structures known as Release Format 2 (RF2). These file structures were introduced in January 2012 to support built-in version tracking and more flexible extensibility mechanisms, including reference sets and packaging of release files into separately identifiable modules. Between its initial release in January 2002 and January 2012, SNOMED CT release files were structured in accordance with an earlier file structure specifications that are now referred to a Release Format 1 (RF1). That release format is deprecated not longer used or supported by SNOMED International.
{% endhint %}
