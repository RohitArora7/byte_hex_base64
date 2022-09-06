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
b64 = base64.b64encode(bytes.fromhex(bh)).decode()
print(b64)

python base64 > hex
s2 = base64.b64decode(b64.encode()).hex()
print(s2)


byte/binary > base64
encoded = binascii.b2a_base64(byte, newline=False)

base64 > byte/binary 
print(binascii.a2b_base64(encoded)) 
```
