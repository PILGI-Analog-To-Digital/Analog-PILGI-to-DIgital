# machine learning in practice 개발 계획

[Copy of Meeting Notes](machine%20learning%20in%20practice%20%E1%84%80%E1%85%A2%E1%84%87%E1%85%A1%E1%86%AF%20%E1%84%80%E1%85%A8%E1%84%92%E1%85%AC%E1%86%A8%207f824082bc6143b997998ba234efb592/Copy%20of%20Meeting%20Notes%2081d6fa0831a44aa5801dd6f04967f145.csv)

## 0. 브레인 스토밍.

- 서울말 ←→ 방언?
- txt → 손글씨
- OCR 손글씨→txt
- 헬스 자세 교정기
- 수업 필기한 자료 문서화
- input(main(깔끔한 수학기호 + DA), sub(손글시)) ⇒ Late

## 0.5 기존 사례 연구

- 네이버 SmartPlace
    - 

![Untitled](machine%20learning%20in%20practice%20%E1%84%80%E1%85%A2%E1%84%87%E1%85%A1%E1%86%AF%20%E1%84%80%E1%85%A8%E1%84%92%E1%85%AC%E1%86%A8%207f824082bc6143b997998ba234efb592/Untitled.png)

- 구글
    
    [문제점.pdf](machine%20learning%20in%20practice%20%E1%84%80%E1%85%A2%E1%84%87%E1%85%A1%E1%86%AF%20%E1%84%80%E1%85%A8%E1%84%92%E1%85%AC%E1%86%A8%207f824082bc6143b997998ba234efb592/%EB%AC%B8%EC%A0%9C%EC%A0%90.pdf)
    
    - 문단이 나눠지지 않음.

## 1. 문제 정의

- 이름 : PILGI Analog To Digital
- input : Image ( 수학 과제, 수업 필기)

![Untitled](machine%20learning%20in%20practice%20%E1%84%80%E1%85%A2%E1%84%87%E1%85%A1%E1%86%AF%20%E1%84%80%E1%85%A8%E1%84%92%E1%85%AC%E1%86%A8%207f824082bc6143b997998ba234efb592/Untitled%201.png)

- output : txt, LaTex, Image 별 다른 OUTPUT을 갖음
- 과정
    1. TEXT → (CHARCTER, CONTENT, 띄어쓰기 여부, 문단 바꾸기 여부)
        1. 글자 크기 DEFAULT
        2. 시작 위치 (x,y) 좌표에다가 해당 TXT 내용 뿌림.
    2. DRAWING → (X, Y, X_SIZE, Y_SIZE)
        1. DETECTION 모델
    3. LATEX CHARACTER ⇒ 실제 기호
        1. 
    
    DETECTOR 모델과, OCR 모델 
    
    - DETECTION LAYER로 해당 PIXEL과 CLASS를 얻음
    - DRAWING CLASS의 경우, 그대로 저장.
    - CHARACTER CLASS의 경우, OCR 모델을

## 2. 설계

- Data 수집
    - Data Augmentation
    - labeling 으로 직접 데이터 만들기
    - computer stanadard character
- Model
    - segmentation → 어떤 픽셀이 어떤 카테고리에 속하는지 분석
        - **Semantic Segmentation** model : U-net
    - image to text (OCR)
    - model save
    - transfer learning
- 문서 작업
    - github read me.
    - 회의록
- ~~결과 수정 feedback ( 가능하면?)~~
    - ㅁㅁ

다음 시간까지 강의듣고,  segmentation, transfomer, 

## 3. 구현

## 4. 테스트

## 5. 배포