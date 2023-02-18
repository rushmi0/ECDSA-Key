# WIF Private Key

WIF มาจากคำว่า Wallet Import Format เป็นรูปแบบมาตรฐาน Private Key สำหรับ Bitcoin เพราะด้วยรูปลักษณ์ Private Key เดิมๆ แล้วเป็นเลขฐาน16 จุดหนึ่ง มันข้อนข้างยากดูยากมาก ๆ WIF Key จึงทำมาเพื่อให้รูปลักษณ์มันดูง่าย ขึ้น ช่วยลดความผิดพลาดจากการกรอก Private Key ผิด


## ส่วนประกอบและขั้นตอนการสร้าง WIF Key

## 1. Prefix

เป็นตัวกำหนดว่า Private Key นี้ใช้สำหรับ Network อะไร
- [Mainnet] = 0x80
- [Testnet] = 0xEF

## 2. Private Key 
เราจะสุ่มตัวเลขมาชุดหนึ่ง นำตัวเลขนั้นไป Hash ด้วย Sha256
- ตัวเลขสุ่ม
```sh
98528754942310573635743257995792764542959923852024254930116003798007826807869
```
- เมื่อ Hash ด้วย Sha256
```sh
c51a52e294165cfde3342e8c12c5f3370d29d12401c03803fe34de78c80b1804
```
## 3. Compression
เป็นตัวกำหนดว่า Private Key นี้ใช้สำหรับสร้าง Public Key แบบบีบอัด ส่วนนี้เป็นตัวเลือกครับ จะใช้หรือไม่ใช้ก็ได้ ไม่บังคับ
- [Compressed] = 0x01
