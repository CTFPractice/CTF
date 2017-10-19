Crypto
===
Hint: Caeser Cipher

![](https://i.imgur.com/kaTBuaY.png)

直接丟入線上的[Caeser Cipher Decoder](https://www.xarg.org/tools/caesar-cipher/)，把keyspace調成19就能拿到FLAG了。

或者自己刻一支程式：
```python=
#caesar_decode.py
ciphertext = "IylhrHSSJAM{MaoceAlxUGBZKLphaLxc}"
x = ciphertext[0]

for keyspace in range(-(ord(x)-65),91-ord(x)):
	for i in ciphertext:
		if (ord(i)>=65 and ord(i)<=90):
			print(chr((ord(i)+keyspace-65)%26+65), end="")
		elif (ord(i)>=97 and ord(i)<=122):
			print(chr((ord(i)+keyspace-97)%26+97), end="")
		else:
			print(i, end="")
	print()

```
