Training: Crypto - Caesar I
===
Hint: Caesar Cipher

可以直接丟進線上的[Caesar cipher decryption tool](https://www.xarg.org/tools/caesar-cipher/)。

或是手刻一個：
```python=
# caesar_decocde.py
ciphertext = "GUR DHVPX OEBJA SBK WHZCF BIRE GUR YNML QBT BS PNRFNE NAQ LBHE HAVDHR FBYHGVBA VF UEVPPABSVOUB"

for keyspace in range(0,26):
	for i in ciphertext:
		if (ord(i)!=32):
			print(chr((ord(i)+keyspace-65)%26+65), end="")
		else:
			print(' ', end="")
	print()
```

執行後可以找到Solution。
![](https://i.imgur.com/LZI25GW.png)