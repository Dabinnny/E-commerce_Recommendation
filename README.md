# E-Commerce 플랫폼 데이터 활용 추천 시스템 구축

</br> 

## ✔️ E-Commerce 산업 특성

<div align="center">
<img src="https://user-images.githubusercontent.com/90162819/161546886-7e15bdb3-5778-49ef-ad15-ac68cd12eed5.png" width="600"></div>

</br> 

- 커머스 사이트는 별점이나 평점과 같은 직접적인 정보를 받기 어렵기 때문에 Implicit Feedback(장바구니, 좋아요,  
 클릭수, 검색수 등)와 사용자의 활동 로그 데이터를 활용
- 가격, 브랜드, 카테고리와 같은 Metadata의 영향력이 높음
- 매 시즌마다 상품들이 지속적으로 바뀌기 때문에 Cold-Start 문제 및 사용자의 행위패턴을 분석하기 위해 최신성이 중요

</br> 

## ✔️ Data 

(1) 패션 커머스 플랫폼 데이터(익명화, 샘플링) 
- **기간** : 2021. 06. 03. ~ 2021. 08. 04.
- **로그수** : 5,880,407개  
- **item수** : 283,326개  
- **user수** : 254,958  

</br> 

(2) 사용자, 상품, 로그 데이터 활용  

|**User**|id,  birth_day,  gender|
|:-------:|:-------:|
|**Product**|**id,  name,  category,  price,  brand**|
|**Event**|**session_id,  timestamp,  device,  region,  click,  like,  add_to_cart,  purchase**|  

</br> 

(3) 데이터베이스 연동 
- **PostgreSQL**, DBeaver 활용

</br> 
</br> 

## ✔️ 1. Best Item 추천  

- 세부 내용 및 코드 : [바로가기](https://github.com/Dabinnny/E-commerce_Recommendation/blob/main/best_recommendation.ipynb)  

- 추천 별 그룹화 및 Query 추출  
(1) Best의 대상이 되는 그룹의 정의  
(2) 각 그룹마다 특성화된 scoring 적용

<div align="center">
<img src="https://user-images.githubusercontent.com/90162819/161704759-9868af17-e659-4303-8604-437d4deefe8a.png" width="700"></div>  

</br> 
</br> 

## ✔️ 2. 연관 상품 추천 

- 세부 내용 및 코드 : [바로가기](https://github.com/Dabinnny/E-commerce_Recommendation/blob/main/relatedItem_recommendation.ipynb)  

- 추천 별 그룹화 및 Query 추출  
(1) cosine 유사도를 활용하여 연관성 고려  
(2) 가중치 할당 (대중적인 아이템은 조회나 접근 횟수가 많아 단순 count수가 많으므로 log값 적용)  
(3) 아이템들의 연관성 추출 기준은 application에 맞게 선택 (사용자, 세션, 인접)

<div align="center">
<img src="https://user-images.githubusercontent.com/90162819/161703892-db26bdc5-a732-42c4-8217-3c724d1bc26c.png" width="700"></div>  

</br> 
</br> 

## ✔️ 3. 개인화 맞춤 추천 

- 세부 내용 및 코드 : [바로가기](https://github.com/Dabinnny/E-commerce_Recommendation/blob/main/personalized_recommendation.ipynb)

- 추천 별 그룹화 및 Query 추출  
(1) 특정 사용자 history를 활용하여 활동 이력 로그 추출 
(2) 사용자 별 취향이 유사한 사용자 집합 추출

<div align="center">
<img src="https://user-images.githubusercontent.com/90162819/161711489-06e6beaa-5187-4388-a2de-0d5acda84bbb.png" width="450"></div>  


</br> 
</br> 
</br> 
</br> 
</br> 
</br> 

> reference  
  - 이 프로젝트는 번개장터 CTO 이동주님의 추천시스템 강의를 참고하였습니다.






