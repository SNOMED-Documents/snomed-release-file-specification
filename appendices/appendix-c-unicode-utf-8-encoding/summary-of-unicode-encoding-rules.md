# Summary of Unicode Encoding Rules

Character encoding

* ASCII characters (in the range 0-127) are encoded as a single byte.
* Greek, Hebrew, Arabic and most accented European characters are encoded as two bytes;
* Other characters are encoded as three bytes;
* The individual characters are encoded according to the following rules.

### Single byte encoding

Characters in the range 'u+0000' to 'u+007f' are encoded as a single byte.

Table 1: UTF-8 Single Byte Encoding

<div align="left"><figure><img src="../../.gitbook/assets/Image 12-08-2025 at 10.40.jpg" alt=""><figcaption></figcaption></figure></div>

### Two byte encoding

Characters in the range 'u+0080' to 'u+07ff' are encoded as two bytes.

Table 2: Two byte encoding

<div align="left"><figure><img src="../../.gitbook/assets/Image 12-08-2025 at 10.42.jpg" alt=""><figcaption></figcaption></figure></div>

### Three byte encoding

Characters in the range 'u+0800' to 'u+ffff' are encoded as three bytes:

Table 3: UTF-8 Three Byte Encoding

<div align="left"><figure><img src="../../.gitbook/assets/Image 12-08-2025 at 10.43.jpg" alt=""><figcaption></figcaption></figure></div>

## Notes on encoding rules

The first bits of each byte indicate the role of the byte. A zero bit terminates this role information. Thus possible byte values are:

Table 4: UTF-8 Encoding Rules

<table data-header-hidden><thead><tr><th width="148.08856201171875"></th><th width="130.87933349609375"></th><th></th></tr></thead><tbody><tr><td><strong>Bits</strong></td><td><strong>Byte value</strong></td><td><strong>Role</strong></td></tr><tr><td>0???????</td><td>000-127</td><td>Single byte encoding of a character</td></tr><tr><td>10??????</td><td>128-191</td><td>Continuation of a multi-byte encoding</td></tr><tr><td>110?????</td><td>192-223</td><td>First byte of a two byte character encoding</td></tr><tr><td>1110????</td><td>224-239</td><td>First byte of a three byte character encoding</td></tr><tr><td>1111???</td><td>240-255</td><td>Invalid</td></tr></tbody></table>

## Example encoding

Table 5: UTF-8 Encoding Example

<div align="left"><figure><img src="../../.gitbook/assets/Image 12-08-2025 at 10.47.jpeg" alt=""><figcaption></figcaption></figure></div>
