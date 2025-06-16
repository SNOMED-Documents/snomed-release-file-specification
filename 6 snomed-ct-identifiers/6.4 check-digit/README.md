# 6.4 Check-digit

The final digit of the [SCTID](https://confluence.ihtsdotools.org/display/DOCRELFMT/SCTID+\(data+type\) "Reference term: SCTID \(\(data type\)\)") is a check-digit. 

Users should be required to type [SCTID](https://confluence.ihtsdotools.org/display/DOCRELFMT/SCTID+\(data+type\) "Reference term: SCTID \(\(data type\)\)") values but in some case during design and development it may be necessary to copy or paste identifiers. The objective of the check-digit is to detect the commonest types of error that may occur due to typographical errors on those situations or in other cases where transcription or communication mechanisms may introduce error. Examples may include high-level development such as creating or modifying protocols or pre-specified queries. 

An [SCTID](https://confluence.ihtsdotools.org/display/DOCRELFMT/SCTID+\(data+type\) "Reference term: SCTID \(\(data type\)\)") is checked by using the [Verhoeff check](http://www.augustana.ab.ca/~mohrj/algorithms/checkdigit.html), which is a Dihedral D 5 Check. This detects a higher proportion of common typographical errors than either the IBM or Modulus 11 check. Unlike the Modulus 11 check it is effective on decimal strings longer than ten-digits. Furthermore its value can always be represented as a decimal digit without excluding any values. 

# Related Links

  * See [Check-Digit Computation](6.4.2-Check-digit-Computation_33490102.html) for detailed information about the Verhoeff check-digit algorithm and links to sample program code. 

  * See <http://snomed.org/verhoeff> for a sample web form that can be used to compute a check-digit or check the validity of an [SCTID](https://confluence.ihtsdotools.org/display/DOCRELFMT/SCTID+\(data+type\) "Reference term: SCTID \(\(data type\)\)"). 

