# Crypto04 - 100pts
### Challenge
> Note: Key is in lowercase
[Key](key.txt)
[Cipher](cipher.txt)

### Solution
- Đầu tiên mình sẽ tìm key dựa vào file BTC cung cấp
```
1. The corporation that made Windows 11?
	|x|x|x|?|x|x|x|x|x|
=> MICROSOFT
=> ? = R
2. What 6 character programming language do you know?
	|x|x|?|x|x|n|
=> PYTHON
=> ? = T
3. Which operating system was released on September 17, 1991?
	|x|?|x|x|x|
=> LINUX
=> ? = I

=> Key: RTINFEW
---The key is the name of the creator of this challenge---
```
- Không biết đây có phỉa dụng ý của BTC khi để "The key is the name of the creator of this challenge" hay không nhưng mình đã search "RTINFEW" và tìm được link FB của anh [Lê Nguyễn Tiến Vinh](https://www.facebook.com/lenguyen.tienvinh) rồi từ "Vinh" mình nghĩ đến "Vigenere" cipher
- Tiếp theo mình decode cipher text được cung cấp với key tìm được và kết quả:
```
===Flag cannot be enclosed in "" or {} ===
I am the creator of this crypto challenge, I hope someone will solve it, this is easy level but requires thinking and knowledge about coding. Here I use Vigenere Chiper to create this challenge for you, to solve it you need to find the key to decrypt this code find the flag is crypt0_1s_th3_b3st. Good luck with this challenge! Cordially greet!
```
- Flag:  crypt0_1s_th3_b3st