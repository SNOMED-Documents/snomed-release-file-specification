# RF1 Compatibility and Conversion Tools

In January 2012 the SNOMED International switched from the original Release Format (used for SNOMED CT distribution since 2002), to the more flexible and consistent Release Format 2 (RF2). This means that from that date onward the primary source data for the SNOMED CT International Release is maintained and distributed in the RF2 format.

The SNOMED International recognizes that, while implementers will which to benefit from the features of the new format, there is inevitably a transitional period during which both format are in use. Therefore, the SNOMED International provides the following resources to support users whose system do not yet support SNOMED CT Release Format 2:

* Release Format 1 files will continue to be included in the International Release for a limited period
  * These files are not the authoritative version of SNOMED CT but are generated from the authoritative RF2 data using a software utility developed for this purpose.
  * The resulting RF1 data retains the functionality of the original release data but does not support any of the features of RF2. While all the clinically relevant SNOMED CT hierarchies are identical in both releases, the additional "Metadata Hierarchy" added as part of the RF2 upgrade is not included in the RF1 converted data. In addition there are some cases where Cross Maps
* The RF2 to RF1 Conversion Tool used for generating the RF1 files is also available to all Members and Affiliate Licensees
  * The "RF2 Conversion Tool" is an open source, Java-based, software tool to facilitate the conversion of SNOMED CT files released in RF2 format into RF1 format. The tool provides both a command line utility and a Graphical User Interface (GUI) to facilitate configuration, progress tracking and the maintenance of additional data whenever it is not available as part of an RF2 release.
  * The limitations of RF2 to RF1 conversion (noted above) will also apply to conversion undertaken using this tool. To enable the conversion to be completed successfully in a way that retains and replaces Identifiers consistently for the RF1 environment a set of auxiliary files (the "RF1 Compatibility Package") is also required.

The "RF2 to RF1 Conversion Tool" and the "RF1 Compatibility Package" are available for Members and Affiliates to download in the same way as the SNOMED CT International Release.

{% hint style="danger" %}
**Caution!**

These resources and tools are intended for use during a transitional period and should not be considered as a long term alternative to migration to support direct use of RF2 data within applications. As SNOMED CT continues to evolve more of the specific feature of RF2 will be used to add value to the terminology. Some of the added value delivered by RF2 is soon likely to be regarded as essential for effective solutions to user requirements.
{% endhint %}
