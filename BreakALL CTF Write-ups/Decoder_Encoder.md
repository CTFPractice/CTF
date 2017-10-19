Decoder/Encoder
===
Hint: Base64

![](https://i.imgur.com/xlp5IDt.png)

把字串丟進[Base64 Decoder](https://www.base64decode.org/)，直接拿到FLAG。

或者，可以自己刻一支程式：
```python=
# base64_decode.py
import base64

s = "QnJlYWtBTExDVEZ7VDNxejZIZk9XTWUyOERGM2xTTVJ9"
s = base64.b64decode(s)
print(s)
```

run一下就能拿到FLAG了。
```
$ python base64_decode.py
b'BreakALLCTF{xxxxxxxxxxxxxxxxxxxx}'
```
