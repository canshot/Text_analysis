
# 1.IMDB review sentiment analysis
## (1) Bag of Words
## (2) Word2Vec

# 2. Naver movie review sentiment analysis

# 3. Cosmetic review sentiment analysis

● 사전 주제 목표 : 화장품 리뷰 감성분석

● 데이터 수집
- 화장품 정보 플랫폼(글로우픽)에서 고객 후기와 평점을 크롤링한다.

● 분석 알고리즘
- konlpy를 사용하여 한글 형태소 분석을 한 후, sentiment 분석을 한다.
- Okt로 한글 형태소 분석을 한다.

● 분석 의의
- 화장품 리뷰 기반으로 화장품의 긍정, 부정 감성예측
- 화장품 회사의 리뷰 데이터 확보의 중요성
- 향후 화장품 추천 모델에 적용

● 한글 자연어처리 포인트

## 1) 이모티콘(😍) 제거
  - 이모티콘은 주로 문장 맨 끝에 있다.
  - 파이썬 코드1 : 이모티콘 중에 없어지는 것도, 안 없어지는 것도 있다.
  - 파이썬 코드2 : 이모티콘과 단어가 붙어있을 경우 붙어있는 단어도 제거된다…
## 2) 하트 제거(♡♥)   ->   .하트.
## 3) 👍 ->   .굿굿.
## 4) 오타 수정(한글 형태 파괴 주범들)
  - 기름기 좌ㄹ좌ㄹ -> 기름기 좔좔
  - 와우 피부인지 사막인지 앍ㅎ챠냗ㅃㄴㄹ호갸늌 -> 삭제
  - 띄어쓰기 무시 : 샘플 받아서쓰고있는데뭐랄까은근겉도는느낌이랄까요시간좀지나면흡수되긴하는데엄청촉촉한것두아니고  -> 띄어쓰기화!

