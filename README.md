# E-Commerce 플랫폼 데이터 활용 추천 시스템 구축

</br> 

## ✔️ E-Commerce 산업 특성

<div align="center">
<img src="https://user-images.githubusercontent.com/90162819/161546886-7e15bdb3-5778-49ef-ad15-ac68cd12eed5.png" width="600"></div>

</br> 

- 커머스 사이트는 별점이나 평점과 같은 직접적인 정보를 받기 어렵기 때문에 Implicit Feedback(장바구니, 좋아요,  
 클릭수, 검색수 등)와 사용자의 활동 로그 데이터를 활용
- 가격, 브랜드, 카테고리의 Metadata의 영향력이 높음
- 매 시즌마다 상품들이 지속적으로 바뀌기 때문에 Cold-Start 문제 및 사용자의 행위패턴을 분석하기 위해 최신성이 중요

</br> 

## ✔️ Data 특성 

(1) 패션 커머스 플랫폼 데이터(익명화, 샘플링) 
- **기간** : 2021. 06. 03. ~ 2021. 08. 04.
- **로그수** : 5,880,407개  
- **item수** : 283,326개  
- **user수** : 254,958  

(2) 사용자, 상품, 로그 데이터 활용  

|**User**|id, birth-day, gender|
|:-----:|:-----:|
|**Product**|id, name, category, price, brand|
|**Event**|session_id, timestamp, device, region, click, like, add_to_cart, purchase|  

(3) 데이터베이스 연동 
- **PostgreSQL**, DBeaver 활용

</br> 

## ✔️ 1. Best Item 추천  

- 진행 내용 : [바로가기](https://github.com/Dabinnny/E-commerce_Recommendation/blob/main/best_recommendation.ipynb)  

- 추천 별 그룹화 및 Query 추출
(1) Best의 대상이 되는 그룹의 정의  
(2) 각 그룹마다 특성화된 scoring 적용

<div align="center">
<img src="https://user-images.githubusercontent.com/90162819/161695535-a76b0745-8d5c-4385-a7eb-1ddcec45e81a.png" width="600"></div>  



## ✔️ 2. 연관 상품 추천 

- 진행 내용 : [바로가기](https://github.com/Dabinnny/E-commerce_Recommendation/blob/main/relatedItem_recommendation.ipynb)

<div align="center">
<img src="https://user-images.githubusercontent.com/90162819/161546886-7e15bdb3-5778-49ef-ad15-ac68cd12eed5.png" width="600"></div>  



## ✔️ 3. 개인화 맞춤 추천 

- 진행 내용 : [바로가기](https://github.com/Dabinnny/E-commerce_Recommendation/blob/main/personalized_recommendation.ipynb)

<div align="center">
<img src="https://user-images.githubusercontent.com/90162819/161546886-7e15bdb3-5778-49ef-ad15-ac68cd12eed5.png" width="600"></div>  






