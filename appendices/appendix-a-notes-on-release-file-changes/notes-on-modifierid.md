# Notes on modifierId

These notes provide additional information about the modifierId column in the Relationship File. The modifierId column was included in the specification of the relationships file in the expectation that it would in future distinguish between different types of description logic axiom. However, in practice it has not been used. Different approaches to enhanced use of description logic are under consideration and it now seems unlikely that this column will be used as originally intended.  Therefore, until further notice it is recommended that the contents of this column should be ignored.

The following notes were included in the original specification of modifierId and are retained here for consistency.

{% hint style="info" %}
**Original release notes on modifierId**

The  [modifierId](../appendix-b.-specification-reference-information/m/modifierid-field.md) field will initially be set to [900000000000451002 |Some|](http://snomed.info/id/900000000000451002) to keep compatibility with the RF1 release. Widening the range of this field to include other values (such as |All|) will in future increase the expressive power of SNOMED CT. However, this is likely to come at the cost of an increase in reasoning complexity, leading to potential issues for classification tooling.

Notes:&#x20;

1. The modiferId field has been included at this stage as the RF2 format is likely to be stable for at least a five year period, without addition or deletion of fields. Within that period it is anticipated that other modifierId values will be added. Therefore, although not fully implemented at this stage, this field has been included in the initial RF2 specification as it represents an integral part of the Description Logic used by SNOMED CT.
2. Any expansion of SNOMED CT to include relationships with a  modifierId set to a value other than [900000000000451002 |Some|](http://snomed.info/id/900000000000451002) will be discussed with Members prior to introduction.
3. Changes have been made to the "Immutability" values shown in the above table in the 2014-07-31 version. These changes reflect the fact that the values in the following columns of a uniquely identified relationship have occurred in historical data and in these cases tracking the history of these changes is of greater value that insisting on immutability.&#x20;
   * relationshipGroup: The number can change though the logical content of the group represented should not change. Additionally no significance should be read into the relationshipGroup value of an inactive relationship;
   * characteristicType: This has changed in historical data but should not change in future;
   * modifierId: Since there is currently only one value for this no changes are possible but if the permitted values are extended as suggested above then it is likely that changes would be required.
{% endhint %}

\
