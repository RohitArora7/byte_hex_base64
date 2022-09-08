# byte_hex_base64

```bash
 
byte=b'z\xe6\xac\x8e\x9d\x81\xc0jXNb\xee\xf9Tw\xf2\xed\x9e\xd0\xa4\xbc=\xed\xd1\xd3\xb3#\xbbk\xfa\rn'
-------hex--------
7ae6ac8e9d81c06a584e62eef95477f2ed9ed0a4bc3dedd1d3b323bb6bfa0d6e
-------base64 string encoded--------
b'euasjp2BwGpYTmLu+VR38u2e0KS8Pe3R07Mju2v6DW4='



hex > base64 string encoded

7ae6ac8e9d81c06a584e62eef95477f2ed9ed0a4bc3dedd1d3b323bb6bfa0d6e

euasjp2BwGpYTmLu+VR38u2e0KS8Pe3R07Mju2v6DW4=



JS - hex > base64 
var base64String = Buffer.from(a, 'hex').toString('base64')
JS - base64 > hex  
var hexString = Buffer.from(base64String, 'base64').toString('hex')
 
 

python hex > base64 
import base64
b64 = base64.b64encode(bytes.fromhex(bh)).decode()
print(b64)

python base64 > hex
s2 = base64.b64decode(b64.encode()).hex()
print(s2)


byte/binary > base64
import binascii
encoded = binascii.b2a_base64(byte, newline=False)

base64 > byte/binary 
print(binascii.a2b_base64(encoded)) 
```




chr() is used for converting an Integer to a Character\
ord() is used to do the reverse, i.e, convert a Character to an Integer\

We can also pass Integers represented in other common bases, such as Hexadecimal format (base 16) to chr() and ord().\
In Python, we can use Hexadecimal by prefixing an integer with 0x, provided it is within the 32/64 bit range for integer values.\
We pass the integer 18 in hexadecimal format to chr(), which returns a hexadecimal 0x12. We pass that to chr() and use ord() to get back our integer.

```bash
>>> print(chr(65)) 
'A'
>>> print(ord('A')) 
'65'
>>> print(hex(18))
'0x12'
>>> print(chr(0x12))
'\x12'
>>> print(ord('\x12'))
18
>>> print(int('\x12'))
18
```

[ 218, 196, 85, 62, 50 ........] 
[ b'\x10\x07Att2\x08T\x18q\x11\x91 .........]
[F3GZEAM4GCkBRhhBU ........] 

```bash
\x10 is is not the hex representation of decimal 218, Some error in translation of datatypes.
```





161
```bash
print(ord('\xa1'))

console.log('\xa1'.charCodeAt(0))
```

```bash

number to hex
hexString = yourNumber.toString(16);

hex to number
yourNumber = parseInt(hexString, 16)

```

```bash
decimal to hex
function buf2hex(buffer) { // buffer is an ArrayBuffer
  // create a byte array (Uint8Array) that we can use to read the array buffer
  const byteArray = new Uint8Array(buffer);
  
  // for each element, we want to get its two-digit hexadecimal representation
  const hexParts = [];
  for(let i = 0; i < byteArray.length; i++) {
    // convert value to hexadecimal
    const hex = byteArray[i].toString(16);
    
    // pad with zeros to length 2
    const paddedHex = ('00' + hex).slice(-2);
    
    // push to array
    hexParts.push(paddedHex);
  }
  
  // join all the hex values of the elements into a single string
  return hexParts.join('');
}

// EXAMPLE:
const buffer = new Uint8Array([ 4, 8, 12, 16 ]).buffer;
console.log(buf2hex(buffer)); // = 04080c10
```
