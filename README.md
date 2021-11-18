# PILGI Analog To Digital

[Meeting Notes](PILGI%20Analog%20To%20Digital%207f824082bc6143b997998ba234efb592/Meeting%20Notes%2081d6fa0831a44aa5801dd6f04967f145.csv)

[엔지니어 정보](PILGI%20Analog%20To%20Digital%207f824082bc6143b997998ba234efb592/%E1%84%8B%E1%85%A6%E1%86%AB%E1%84%8C%E1%85%B5%E1%84%82%E1%85%B5%E1%84%8B%E1%85%A5%20%E1%84%8C%E1%85%A5%E1%86%BC%E1%84%87%E1%85%A9%20eef8f2fb4f24449ca24ba169a21128a2.csv)

📒[개발 노트 링크]() 

🐈[github 링크](https://github.com/PILGI-Analog-To-Digital/Analog-PILGI-to-DIgital#analog-pilgi-to-digital) 

## 0. 선행 연구

- 네이버 SmartPlace
    - 그림, 수식 표현에 제한

![Untitled](PILGI%20Analog%20To%20Digital%207f824082bc6143b997998ba234efb592/Untitled.png)

- 구글
    
    [문제점.pdf](PILGI%20Analog%20To%20Digital%207f824082bc6143b997998ba234efb592/%EB%AC%B8%EC%A0%9C%EC%A0%90.pdf)
    
    - 문단이 나눠지지 않음.
    - pdf는 인식이 잘 되지만 손 글씨는 잘 인식하지 못함.

## 1. 문제 정의

- 이름 : PILGI Analog To Digital
- IDEA :
    
    → 강의 듣는데 자신의 글씨를 알아볼 수 없다. 
    
    → 깔끔하게 저장할 수 있는 model 필요!
    
- input : Image ( 수학 과제, 수업 필기)

![Untitled](PILGI%20Analog%20To%20Digital%207f824082bc6143b997998ba234efb592/Untitled%201.png)

- output : txt, LaTex, Image 별 다른 OUTPUT을 갖음

## 2. 구조

- 과정
    1. TEXT → (CHARCTER, CONTENT, 띄어쓰기 여부, 문단 바꾸기 여부)
        1. 글자 크기 DEFAULT
        2. 시작 위치 (x,y) 좌표에다가 해당 TXT 내용 뿌림.
    2. DRAWING → (X, Y, X_SIZE, Y_SIZE)
        1. DETECTION 모델
    3. LATEX CHARACTER ⇒ 실제 기호
        1. 
- DETECTOR 모델과, OCR 모델
    - DETECTION LAYER로 해당 PIXEL과 CLASS를 얻음
    - DRAWING CLASS의 경우, 그대로 저장.
    - CHARACTER CLASS의 경우, OCR 모델을

## 3. 모델의 차별점

- GAN을 이용한 Data Argumentation
    - 
- user 맞춤형, 약간의 overfitting
    - 루게릭 병
- [Data Labeling 강의 수강](http://aidata.elancer.co.kr/student/write.php?lid=MjA1)
    
    ![Untitled](PILGI%20Analog%20To%20Digital%207f824082bc6143b997998ba234efb592/Untitled%202.png)
    

## 4. 테스트 및 배포

- OCR의 중간에 user가 feedback 가능하도록
- 나중에