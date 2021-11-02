# Crypto06 - 150pts
### Challenge
>Back to 2016.
You should submit: WhiteHat{sha1(lowercase(flag))}
[File](cipher.txt)
### Solution
- Đề cho một đoạn cipher Multi-tap Phone (SMS).
- Decode bằng tool sẽ ra đoạn plan text bị khuyết:
```
Đây là phần flag nếu decode bằng tool: FLAG GHS/HGS/IPR/IRP/IS ALWAYS BEDDE/BEDF/BFF THE S N OF/ODE/OED THAI BINH
```
- Ta có thể đoán những từ có nghĩa thì sẽ ra và sẽ còn 2 từ chưa rõ như sau:
```
FLAG IS ALWAYS BEDDE/BEDF/BFF THE S N OF THAI BINH
```
- Tới đây ta quay lại cipher text:
```
223333 => BEDDE/BEDF/BFF.
22 => B
Tưởng tượng mình đang dùng cục gạch thì 3333 => 3
Vậy 223333 => B3
```
- Tương tự với "S N"
```
7777066 => S N
Tách ra:
7777 => S
0 => 0 
66 => n
Vậy 7777066 =>S0N
```
- Lowcase flag: always b3 the s0n of thai binh
