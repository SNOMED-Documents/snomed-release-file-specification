# Appendix C. Unicode UTF-8 encoding

UTF-8 is an efficient encoding of [Unicode](appendix-b.-specification-reference-information/u/unicode.md) character - String that recognizes the fact that the majority of text-based communications are in ASCII. It therefore optimizes the encoding of these characters.

Unicode is preferred to ASCII because it permits the inclusion of accents, scientific symbols and characters used in languages other than English. The UTF-8 format is a standard encoding that provides the most efficient means of encoding 16-bit Unicode characters in cases where the majority of characters are in the ASCII range. Both UTF-8 and the alternative UTF-16 encoding are supported by all widely used operating systems and major applications. UTF-8 was adopted is an [IETF Internet Standard](https://tools.ietf.org/html/rfc3629) (it was initially adopted by IETF in 1996 to restrict some code values in 1998 and 2003). In 2008 UTF-8 became the most widely used for of encoding in web pages.

SNOMED CT uses the UTF-8 representation of characters in terms and other text fields.

{% hint style="info" %}
Note that SNOMED CT does not use, or require use of, the [Byte Order Mark (BOM)](https://en.wikipedia.org/wiki/Byte_order_mark) specified by the Unicode standard because all SNOMED CT release files use UTF-8.
{% endhint %}

## Summary of Unicode Encoding Rules

Character encoding

* ASCII characters (in the range 0-127) are encoded as a single byte.
* Greek, Hebrew, Arabic and most accented European characters are encoded as two bytes;
* Other characters are encoded as three bytes;
* The individual characters are encoded according to the following rules.

### Single byte encoding

Characters in the range 'u+0000' to 'u+007f' are encoded as a single byte.

**UTF-8 Single Byte Encoding**

<div align="left"><figure><img src="../.gitbook/assets/Image 12-08-2025 at 10.40.jpg" alt=""><figcaption></figcaption></figure></div>

### Two byte encoding

Characters in the range 'u+0080' to 'u+07ff' are encoded as two bytes.

**Two byte encoding**

<div align="left"><figure><img src="../.gitbook/assets/Image 12-08-2025 at 10.42.jpg" alt=""><figcaption></figcaption></figure></div>

### Three byte encoding

Characters in the range 'u+0800' to 'u+ffff' are encoded as three bytes:

**UTF-8 Three Byte Encoding**

<div align="left"><figure><img src="../.gitbook/assets/Image 12-08-2025 at 10.43.jpg" alt=""><figcaption></figcaption></figure></div>

## Notes on encoding rules

The first bits of each byte indicate the role of the byte. A zero bit terminates this role information. Thus possible byte values are:

**UTF-8 Encoding Rules**

<table><thead><tr><th width="148.08856201171875">Bits</th><th width="130.87933349609375">Byte value</th><th>Role</th></tr></thead><tbody><tr><td>0???????</td><td>000-127</td><td>Single byte encoding of a character</td></tr><tr><td>10??????</td><td>128-191</td><td>Continuation of a multi-byte encoding</td></tr><tr><td>110?????</td><td>192-223</td><td>First byte of a two byte character encoding</td></tr><tr><td>1110????</td><td>224-239</td><td>First byte of a three byte character encoding</td></tr><tr><td>1111???</td><td>240-255</td><td>Invalid</td></tr></tbody></table>

## Example encoding

**UTF-8 Encoding Example**

<div align="left"><figure><img src="../.gitbook/assets/Image 12-08-2025 at 10.47.jpeg" alt=""><figcaption></figcaption></figure></div>
