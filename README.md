# PILGI Analog To Digital

๐[Meeting Notes](PILGI%20Analog%20To%20Digital%207f824082bc6143b997998ba234efb592/Meeting%20Notes%2081d6fa0831a44aa5801dd6f04967f145.csv)


๐งโ๐ป[์์ง๋์ด ์ ๋ณด](PILGI%20Analog%20To%20Digital%207f824082bc6143b997998ba234efb592/%E1%84%8B%E1%85%A6%E1%86%AB%E1%84%8C%E1%85%B5%E1%84%82%E1%85%B5%E1%84%8B%E1%85%A5%20%E1%84%8C%E1%85%A5%E1%86%BC%E1%84%87%E1%85%A9%20eef8f2fb4f24449ca24ba169a21128a2.csv)

๐[๊ฐ๋ฐ ๋ธํธ ๋งํฌ](https://encouraging-saltopus-3be.notion.site/PILGI-Analog-To-Digital-7f824082bc6143b997998ba234efb592) 

๐[github ๋งํฌ](https://github.com/PILGI-Analog-To-Digital/Analog-PILGI-to-DIgital#analog-pilgi-to-digital) 

## 0. ์ ํ ์ฐ๊ตฌ

- ๋ค์ด๋ฒ SmartPlace
    - ๊ทธ๋ฆผ, ์์ ํํ์ ์ ํ

![Untitled](PILGI%20Analog%20To%20Digital%207f824082bc6143b997998ba234efb592/Untitled.png)

- ๊ตฌ๊ธ
    
    [๋ฌธ์ ์ .pdf](PILGI%20Analog%20To%20Digital%207f824082bc6143b997998ba234efb592/%EB%AC%B8%EC%A0%9C%EC%A0%90.pdf)
    
    - ๋ฌธ๋จ์ด ๋๋ ์ง์ง ์์.
    - pdf๋ ์ธ์์ด ์ ๋์ง๋ง ์ ๊ธ์จ๋ ์ ์ธ์ํ์ง ๋ชปํจ.

## 1. ๋ฌธ์  ์ ์

- ์ด๋ฆ : PILGI Analog To Digital
- IDEA :
    
    โ ๊ฐ์ ๋ฃ๋๋ฐ ์์ ์ ๊ธ์จ๋ฅผ ์์๋ณผ ์ ์๋ค. 
    
    โ ๊น๋ํ๊ฒ ์ ์ฅํ  ์ ์๋ model ํ์!
    
- input : Image ( ์ํ ๊ณผ์ , ์์ ํ๊ธฐ)

![Untitled](PILGI%20Analog%20To%20Digital%207f824082bc6143b997998ba234efb592/Untitled%201.png)

- output : txt, LaTex, Image ๋ณ ๋ค๋ฅธ OUTPUT์ ๊ฐ์

## 2. ๊ตฌ์กฐ

- ๊ณผ์ 
    1. TEXT โ (CHARCTER, CONTENT, ๋์ด์ฐ๊ธฐ ์ฌ๋ถ, ๋ฌธ๋จ ๋ฐ๊พธ๊ธฐ ์ฌ๋ถ)
        1. ๊ธ์ ํฌ๊ธฐ DEFAULT
        2. ์์ ์์น (x,y) ์ขํ์๋ค๊ฐ ํด๋น TXT ๋ด์ฉ ๋ฟ๋ฆผ.
    2. DRAWING โ (X, Y, X_SIZE, Y_SIZE)
        1. DETECTION ๋ชจ๋ธ
    3. LATEX CHARACTER โ ์ค์  ๊ธฐํธ
        1. 
- DETECTOR ๋ชจ๋ธ๊ณผ, OCR ๋ชจ๋ธ
    - DETECTION LAYER๋ก ํด๋น PIXEL๊ณผ CLASS๋ฅผ ์ป์
    - DRAWING CLASS์ ๊ฒฝ์ฐ, ๊ทธ๋๋ก ์ ์ฅ.
    - CHARACTER CLASS์ ๊ฒฝ์ฐ, OCR ๋ชจ๋ธ์

## 3. ๋ชจ๋ธ์ ์ฐจ๋ณ์ 

- GAN์ ์ด์ฉํ Data Argumentation
    - 
- user ๋ง์ถคํ, ์ฝ๊ฐ์ overfitting
    - ๋ฃจ๊ฒ๋ฆญ ๋ณ
- [Data Labeling ๊ฐ์ ์๊ฐ](http://aidata.elancer.co.kr/student/write.php?lid=MjA1)
    
    ![Untitled](PILGI%20Analog%20To%20Digital%207f824082bc6143b997998ba234efb592/Untitled%202.png)
    

## 4. ํ์คํธ ๋ฐ ๋ฐฐํฌ

- OCR์ ์ค๊ฐ์ user๊ฐ feedback ๊ฐ๋ฅํ๋๋ก
- ๋์ค์