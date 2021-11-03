# Crypto01 - 150pts
### Challenge
> One of my people just learned about coding, I tried but couldn't solve it, please help him for me.
[File](buildcrypt.txt)

### Solution
```
*** Cipher text
3 5TXlTk VbiaXk bl hgX hY maX lbfieXlm TgW fhlm pXee-dghpg XgVkrimbhg mXVagbjnXl.

GTfXW TYmXk Cnebnl 5TXlTk, bm bl hgX hY maX heWXlm mriXl hY VbiaXkl TgW bl UTlXW hg maX lbfieXlm fhghTeiaTUXmbV VbiaXk. Bm bl VhglbWXkXW T pXTd fXmahW hY VkrimhZkTiar, Tl bm bl XTlr mh WXVhWX maX fXllTZX hpbgZ mh bml fbgbfnf lXVnkbmr mXVagbjnXl.

8hk maX lTfX kXTlhg, T 5TXlTk VbiaXk bl hYmXg bgVhkihkTmXW hger bg iTkml hY hmaXk VhfieXq XgVkrimbhg lVaXfXl.
Bg VkrimhZkTiar, T 5TXlTk VbiaXk bl VTmXZhkbsXW Tl T lnUlmbmnmbhg VbiaXk bg pabVa maX TeiaTUXm bg maX ieTbg mXqm bl labYmXW Ur T YbqXW gnfUXk Whpg maX TeiaTUXm.

3WoTgmTZXl hY nlbgZ T 5TXlTk VbiaXk bgVenWX:

HgX hY maX XTlbXlm fXmahWl mh nlX bg VkrimhZkTiar TgW VTg ikhobWX fbgbfnf lXVnkbmr mh maX bgYhkfTmbhg
NlX hY hger T lahkm dXr bg maX XgmbkX ikhVXll
HgX hY maX UXlm fXmahWl mh nlX bY maX lrlmXf VTgghm nlX Tgr VhfiebVTmXW VhWbgZ mXVagbjnXl
KXjnbkXl YXp VhfinmbgZ kXlhnkVXl
8eTZ aXkX, 7TLr 5T7l3k
6blTWoTgmTZXl hY nlbgZ T 5TXlTk VbiaXk bgVenWX:

LbfieX lmknVmnkX nlTZX
5Tg hger ikhobWX fbgbfnf lXVnkbmr mh maX bgYhkfTmbhg
8kXjnXgVr hY maX eXmmXk iTmmXkg ikhobWXl T UbZ VenX bg WXVbiaXkbgZ maX XgmbkX fXllTZX
Vhiirebgd bgmXkgXm
```
- Đầu tiên mình sẽ thử một [tool](https://www.dcode.fr/cipher-identifier) khá hữu ích trên Dcode để loại trừ và nhận biết được loại mã hóa.
- Sau khi thử với Caesar cipher mình ra được plantext:
```
*** Plan text
3 5AEsAr CiphEr is onE oF thE simplEst AnD most wEll-known EnCryption tEChniquEs.

NAmED AFtEr Julius 5AEsAr, it is onE oF thE olDEst typEs oF CiphErs AnD is BAsED on thE simplEst monoAlphABEtiC CiphEr. It is ConsiDErED A wEAk mEthoD oF CryptoGrAphy, As it is EAsy to DECoDE thE mEssAGE owinG to its minimum sECurity tEChniquEs.

8or thE sAmE rEAson, A 5AEsAr CiphEr is oFtEn inCorporAtED only in pArts oF othEr ComplEx EnCryption sChEmEs.
In CryptoGrAphy, A 5AEsAr CiphEr is CAtEGorizED As A suBstitution CiphEr in whiCh thE AlphABEt in thE plAin tExt is shiFtED By A FixED numBEr Down thE AlphABEt.

3DvAntAGEs oF usinG A 5AEsAr CiphEr inCluDE:

OnE oF thE EAsiEst mEthoDs to usE in CryptoGrAphy AnD CAn proviDE minimum sECurity to thE inFormAtion
UsE oF only A short kEy in thE EntirE proCEss
OnE oF thE BEst mEthoDs to usE iF thE systEm CAnnot usE Any CompliCAtED CoDinG tEChniquEs
REquirEs FEw ComputinG rEsourCEs
8lAG hErE, 7ASy 5A7s3r
6isADvAntAGEs oF usinG A 5AEsAr CiphEr inCluDE:

SimplE struCturE usAGE
5An only proviDE minimum sECurity to thE inFormAtion
8rEquEnCy oF thE lEttEr pAttErn proviDEs A BiG CluE in DECiphErinG thE EntirE mEssAGE
Coppylink intErnEt
```
- Flag ngay trước mắt nhưng nó không đơn giản như vậy.
> 8lAG hErE, 7ASy 5A7s3r

- Mình đã bỏ bài này một thòi gian khá lâu cho đến khi tìm ra được key.
- Ban đầu mình đã nghĩ về quy luật viết hoa và cũng đã chuyển hết số về dạng chữ vì mình cũng thấy nó có vẻ đúng với quy luật mã hóa nhưng đều sai bởi chữ và số đang sử dụng 2 key khác nhau.
- Sau đó mình tiến đến hướng đi tìm key cho cả đoạn cipher text.
- Sau khi liệt kê hết các số, chữ cái, đánh số chúng bắt đầu từ 0.
> 0-9 A-Z a-z và đánh stt từng ký tự
- Và dựa vào đoạn plan text phía trên thì mình đã thử cộng 7 vào thứ tự các ký tự ở cipher text và kết quả:
> 7TLr 5T7l3k => EaSy CaEsAr
- Flag: EaSy CaEsAr.
