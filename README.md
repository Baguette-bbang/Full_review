# 제품 요약, 추천, 유사제품 제공 사이트 구축

## [**프로젝트 깃허브링크**](https://github.com/orgs/SSU-2023-OpenSource-Project/repositories)

영민님 : [Baguette-bbang](https://github.com/Baguette-bbang) 201292884

[영민 진행상황](https://www.notion.so/ff2607c6a00b490ca309b7c64a8af13d?pvs=21)

원석님 : [wonsokchoi](https://github.com/wonsokchoi) 20192932

[원석 진행상황](https://www.notion.so/7a362c493b9b40a58c5e38c062c84dbe?pvs=21)
<details>
<summary>- **나의 기본 의견 틀 :** **Trend setter**</summary>
    
    생각해본 주제 : 트렌드를 따라가기 힘들고 같은 주제에 대해 여러 영상들이 쏟아져나오는 시대에 시간이 부족한 현대인을 위한 제품 제공!! 같은 주제에 대한 여러 유튜브 영상이 있는데 주제가 비슷한 영상 찾아서 핵심 키워드 알려주기
    
    1. 기능
    
    - 사용자가 직접 입력한 url을 통해 알려주기
    
    - 미리 정해진 주제에 대한 유행, 핵심 키워드 알려주기
    
    - 어느 유튜브 영상에서 가져왔는지 출처 보여주기
    
    - ex) 패션 이라는 주제에서는 트렌드 컬러, Y2K 패션, 올드머니룩… 등
    
    2. 기술
    
    - 자연어 처리 :  의미없는 단어들을 골라낼 수 있어야 함. gpt api로 처리 가능하긴 할 거 같긴 함…
    
    - 영상 → 스크립트 전환 : 유튜브에서 자동 자막으로 제공하긴 함. 또는https://openai.com/research/whisper 가 있음.
    
    - 여러 영상에서 뽑아낸 스크립트들을 엮에서 QA 형식으로 답을 할 수 있게 하기(랭체인)
    
    3. 형태 : 웹이나 앱
</details>
- **경원님 의견 : Social media detox**
    
    단순히 응용프로그램을 제거하는 방향 보다는 , 기준에 사용하고 있는 것을 어떻게 더 가치있고, 본인이 앱을 사용하려는 purposeLt intention을 인지하고 social media를 활용할 수 있는 방법 고안.
    
    - 현재 social media 에서 자주 보이는 혹은 자주 사용하고 있는 Word들을 학습을 통해서
    
    삶에 도움이 될 수 있는 방향 모색
    
    : -> 다양한 Keyword들 중에서 본인에게 가장 많이 표시되고 보여지는 것들을 학습을 통해서 관련된 취미 혹은
    
    체험등을 제안.
    
    +EX) 옷, 화장품, 이성 , etc. => 최근에 유행하는 trend나 올해의 Color 제안 , 혹은 화장품 사용하는 영상 링크 제공 , 운동 방법 영상 링크 제시
    
    - Langchain 으로 LLM 인터페이스를 사용해서 언어 모델 등을 학습을 하고, 얻은 데이터와 GPT-AP와 다양 한 링크들을 벡터에 저장하고, 이를 활용해서 solution을 제공
    - 이를 통해서 얻을 수 있는 이점 : 무분별하게 사용되는 social_media에 의미를 부여해서 사용하게 함으로써 보 다 생산적인 활동에 참여할 수 있도록 촉진.

내가 원하는 제품과 비슷한 제품이 뭐가 있나.

그 가격과 정보는 어떻게 되고 

유튜버의 평가는 어떻게 되며 

추천할만한 제품인가를 보여줌. → 추천도

가격이 낮은 상품과 높은 상품, 

## 1 주차 회의내용

2023.10.08 / 21:30

**참고 사이트 :** 

- [유튜버 순위](https://playboard.co/)
- [Google trend](https://trends.google.co.kr/trends/)
- [LangChain](https://python.langchain.com/docs/get_started/introduction) : 어떻게 써야 효율적일지 결과를 비교해가면서
요약을 좀 더 쉽게 랭체인 안쓰고 사실 gpt로 진행도 해보고 비교해보면서
    - 예제1 : [빵형의 개발도상국](https://colab.research.google.com/drive/1MlrF0Mo8KHrxcrAeulCP3t9hroc073YN?usp=sharing) : 여러 문서에서 답변하는 챗봇 만들기
    - 예제2 : [빵형의 개발도상국](https://www.youtube.com/watch?v=oGuQwY0AGxg&t=1s) : 내용 물어보면 대답하는 문서 검색 챗봇 만들기

**사용 API :**

- [pytrend](https://pypi.org/project/pytrends/) : 구글트렌드를 api화 과연 합법인가?
- [유튜브 api](https://developers.google.com/youtube/v3/quickstart/python?hl=ko)
- [gpt api](https://platform.openai.com/docs/guides/gpt)

**참고 code :**

- gpt recommendation :
    - [github code](https://github.com/lsjsj92/recommender_system_with_Python/blob/master/009_chatgpt_recsys.ipynb)
    - [blog](https://lsjsj92.tistory.com/657)
- 랭체인 youtube summary
    - [blog1](https://anpigon.tistory.com/400)

**활용 예정 Data: 복합적으로 활용하여 추천**

- 구글 트렌드를 통한 특정 키워드에 대한 조회수 추이
- 특정 키워드에 대한 유튜버들의 순위
- 특정 키워드가 영상에서 얼마나 등장하는지

뽑아온 스크립트에 대해서 다듬는 과정이 필요할 거 같다.

한국어 자연어처리 모델로 스크립트를 최적화하는 과정이 필요할거 같다.

**주기능**

1. 주 키워드에 대한 워드 클라우드 제공(시각적으로 중요 내용 빠르게 파악 가능)
    
    ![Untitled](%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8B%E1%85%AD%E1%84%8B%E1%85%A3%E1%86%A8,%20%E1%84%8E%E1%85%AE%E1%84%8E%E1%85%A5%E1%86%AB,%20%E1%84%8B%E1%85%B2%E1%84%89%E1%85%A1%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8C%E1%85%A6%E1%84%80%E1%85%A9%E1%86%BC%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%20%E1%84%80%E1%85%AE%E1%84%8E%E1%85%AE%E1%86%A8%202fbcf4f31dea42929748ab794be872aa/Untitled.png)
    
2. 키워드에 대한 영상 추천 순위 제공 - 추천 순위를 어떻게 할 것인가? → 딥러닝 모델 → 알아보자→(GPT recommendation 확정)
3. 영상마다의 요약 스크립트 제공 - 유튜브 api 활용 → 영상을 볼것이라면 이 기능을 주력으로 할테지만gpt에 넣고 요약 진행
4. 추천된 영상들의 총 공통적인 요약 내용 정리 - 영상을 보지 않는 사람들 전체적인 흐름만이 중요한 사람들을 위해 → 시간절약측면  gpt에 넣고 요약 진행 (정보나 트렌드 파악)

**부기능**

1. 시각 장애인을 위한 요약 내용 tts서비스
2. 추천 영상에 대한 싫어요, 좋아요 반응을 통한 유저 최적화 추천 영상 제공 
실시간적으로 정보를 제공하는게 과연 쉬울까? 저는 딱! 떠오르지 않는다 방법이… 
3. 영상 관련 채팅 불러오기
4. 필요한 영상 마인드맵 형식으로 저장하기

**기대효과**

- 영상을 누르지 않아도 알 수 있게 스크립트 내용도 요약적으로 알 수 있다.
- 영상을 봐야 알 수 있던 정보들, 트렌드들을 영상을 보지 않아도 알 수 있다. 즉, 어떤 영상을 봐야 최신 트렌드를 잘 따라잡을 수 있는지를 알 수 있다. → 시간낭비 줄어듦
- 하나의 주제(키워드)에 대한 여러 유튜브 영상들에 대한 검증 절차를 거치지 않아도 됨.
- 특정 주제(키워드)에 대한 트렌드를 파악 가능하다. (트렌드 컬러, 유행하는 패션 etc..)
- Youtube Detox

## 2주차 회의내용

2023.10.15 / 21:30

**예정** : 

- 저녁 시간 - (월요일 고정) 매주
    - 경원님
        
        ![Untitled](%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8B%E1%85%AD%E1%84%8B%E1%85%A3%E1%86%A8,%20%E1%84%8E%E1%85%AE%E1%84%8E%E1%85%A5%E1%86%AB,%20%E1%84%8B%E1%85%B2%E1%84%89%E1%85%A1%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8C%E1%85%A6%E1%84%80%E1%85%A9%E1%86%BC%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%20%E1%84%80%E1%85%AE%E1%84%8E%E1%85%AE%E1%86%A8%202fbcf4f31dea42929748ab794be872aa/Untitled%201.png)
        
    - 영민(나)
        
        ![Untitled](%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8B%E1%85%AD%E1%84%8B%E1%85%A3%E1%86%A8,%20%E1%84%8E%E1%85%AE%E1%84%8E%E1%85%A5%E1%86%AB,%20%E1%84%8B%E1%85%B2%E1%84%89%E1%85%A1%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8C%E1%85%A6%E1%84%80%E1%85%A9%E1%86%BC%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%20%E1%84%80%E1%85%AE%E1%84%8E%E1%85%AE%E1%86%A8%202fbcf4f31dea42929748ab794be872aa/Untitled%202.png)
        
    - 원석님
        
        ![Untitled](%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8B%E1%85%AD%E1%84%8B%E1%85%A3%E1%86%A8,%20%E1%84%8E%E1%85%AE%E1%84%8E%E1%85%A5%E1%86%AB,%20%E1%84%8B%E1%85%B2%E1%84%89%E1%85%A1%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8C%E1%85%A6%E1%84%80%E1%85%A9%E1%86%BC%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%20%E1%84%80%E1%85%AE%E1%84%8E%E1%85%AE%E1%86%A8%202fbcf4f31dea42929748ab794be872aa/Untitled%203.png)
        
- 추천 시스템 모델 확정
- 조사한 유튜브 영상 추천 시스템을 위한 모델 선택
    - **Transformer-based Models -[BERT4rec](https://github.com/jaywonchung/BERT4Rec-VAE-Pytorch) , [설명](https://velog.io/@hobbang2/%EC%B6%94%EC%B2%9C%EC%8B%9C%EC%8A%A4%ED%85%9C%EB%85%BC%EB%AC%B8-%EC%BD%94%EB%93%9C-%EC%97%B0%EC%8A%B5-02BERT4REC#06-code--for-my-practice)**
    - **Neural Collaborative Filtering (NCF)**
    - **Wide & Deep Learning**
    - **Recurrent Neural Networks (RNN) / Long Short-Term Memory (LSTM)**
    - DLRM - meta
- 기능적 추가의견 - 없음.
- 수업에서 요구하는 바 상기 - 프로젝트 결정하는데 도움이 많이 될 거 같아서
    - 오픈소스로 참신한 아이디어를 주의깊게 보겠다. (fresh, creative)
    - 완성도 보다는 계획성 을 보겠다.
    - 라이센스 측면도 고려해라.
- 역할 분담
    - 프론트 : 원석님
    - 추천 알고리즘 → 할게 많다. 어디서 막힐지 모른다. 어떤 데이터를 어떻게 활용할지 명확하지 않다. : 영민님
    - 요약 알고리즘, ngrok : 경원님
- 협업용 깃허브 제작
    - repository name :
        - **youtube_breaker - 2표 결정**
        - youtube_detoxer
        - youtube_trend_setter - 1표
- 우리가 하는 짓들이 합법적인가?
    - 라이센스에 대해서 다시 조사하는게 필요할 거 같습니다.
- 다음회의때까지 해야할 것
    - 조사한 라이센스 정리?
    - 기능적 구현도 시작을 해야죠
    

## 3주차 회의내용

2023.11.09 / 18:00

- 웹사이트 제작 시 필요한 데이터
    - 추천 영상
    - 추천 영상에 대한 요약
    - 추천 영상에 대한 순위
- 저장할 데이터가 필요한가?
    - 실시간으로 순위, 트렌드가 바뀌기에 필요없다.
- 웹프레임워크 : flask
    - 참고도서 : 점프 투 플라스크 : [https://wikidocs.net/book/4542](https://wikidocs.net/book/4542)
- 웹사이트 구성
    - 

## 4주차 회의내용

- 날짜 및 시간 : 2023.11.15 / 16:30~18:00
- 장소 : 도서관 세미나실
- 회의 내용 :
    - 각자 진행 및 에러 상황 보고
        - 영민 :
            - 요약 :
                - Youtube API 필터링을 어떻게 할지 - 정해야함.
                - 각 영상에 대한 요약 - 성공
                - total 적으로는 실패. → 계속 시도 예정 - 결과를 본 후 방향성 결정
            - 분석(Recommendation) :
                - 요약 - 거의 완성함.
                - 트렌드(현 상황)
                    - 파이트렌드 사용 어려움.
                    - 돌파방향 생각해야함.
        - 경원 :
            - 진행한 내용
            - 구현해야할 것들
                
                원석이가 만들어준 html  라우팅 함수 작성 ⇒블루프린트 등록하고
                
                json 형식으로 retrun해줄 ⇒ { url , 요약본 } : API  
                
                로그인
                
            - 확장방향성
                
                
                폭 넓은 카테고리를 통한 당양한 사이트를 검색할 수 있는 시간 절약.
                
                구글 검색엔진으로 나온 결과값과 유튜브 영상의 내용 요약한 것을 이용해서
                
                특정한 카테고리에 관련된 제품 추천 
                
                특정 카테고리 ⇒ 자동차 혹은 향수 혹은 
                
                기능 : 
                
                입력받은 특성에 맞는 제품군을 3개 정도로 요약하고 
                
                3개의 제품군으로 사용하는데 ⇒  
                
                1. 몇 개를 추천해서 보여줄 지 
                2. 어떤 방식으로 특성에 맞는 제품을 보여줄 지 
                
                입력 받은 특성에 따른 하위 분류를 3 종류로 
                
                (더  다양한 특성으로 검색을 원하면 트리 구조에서 조금 더 포괄적인 내용으로)
                
                조금 더 일반화된 특성의 제품군으로 
                
                문제점 : 함께 본 상품에 대한 정보에 대한 유사한 측면에 대해서 어떻게 해결할 것인지 
                
                - P
                    
                    
                
                명확하게 하는 것이 중요할 거 같음.
                
                다른 서비스보다 개선의 여지는 있으나 , large lang- model 
                
                어떻게 그게 가능한데 ?에 대한 .. 
                
                하나의 카테고리적인 측면으로 먼저 구현하는 것은 괜찮다고 말씀하시는 것 같음
                
                긍정적인 비디오 몇 개와 부정적인 비디오 몇개를 
                
                ⇒ 비디오 클립 - 글로 된 것을 어떻게 정량화(랭킹할 것인지) 어떻게 변환할 것인지.
                
                제품을 입력할 경우 제품에 대한 리뷰나 이런 거를  
                
                <aside>
                💡 정량화된 값 외에도 정량화할 수 있다는 것이 강점.
                
                </aside>
                
                 즉 정량화된 것으로 제품의 비교를 통한 
                
                 
                
                1. 가장 코어 기술에 대한 것을 중점적으로 할 것이냐
                    
                    → 코어기술이 구현된 사례가 있는지를 
                    
            - 비디오 정량화 기술
                1. 동작인식
                2. 얼굴인식
                3. 음성 및 오디오 분석
        - 원석 :
            - 진행한 내용
                1. 메인 화면 구현
                2. 검색어 입력 받고 영상 표현
            - 구현해야 할 것
                1. 영상 10개 어떤 식으로 보여줄 지, 요약은 어떤 식으로 보여줄 지 구상
                2. 관련 키워드 어떻게 보여줄 지
                3. 로딩화면 구상
            - 받을거
                1. 받을거: 준 키워
    - 대략적인 화면 구상에 대한 회의
        - 홈화면 : 구글처럼 만들기
        - 개인 페이지 만들어서, 내가 검색한 키워드 저장-삭제 가능
        - DB - 검색한 키워드만 저장하자.
        - 메인으로 임펙트 있는 아이디어 있으면 좋겠다. -경원형
            - 영상에 대한 신뢰성(skip 해야하는 정도?) Percentage
    - TODO LIST 작성

## 5주차 회의내용

- 날짜 및 시간 : 2023.11.22 / 16:30~18:00
- 장소 : 도서관 세미나실
- 회의 내용 :
    - 추천을 어떻게 해야할까?
        - 트렌드 파악이 너무 힘들다.
    - 기능 카테고리화
        - 
        
- 입력 형식, 카테고리, 특성입력
    - 유튜브 & 구글에서 정보를 가지고 온다는 특징. 유저정보? 소개자 정보
    - 구글 에서 제품 정보 받고
    - 넓은 카테고리.
    - 일단 유튜브 안봐도 됨.
    - 잘모르는 분야에 대해 유튜브, 구글 평가를 모아서 보여준다? 그런 느낌
    - 검색이 용이하다.
    - 특성 추천

## 교수님 미팅

질문

- 초기 아이디어
    
    ![Untitled](%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8B%E1%85%AD%E1%84%8B%E1%85%A3%E1%86%A8,%20%E1%84%8E%E1%85%AE%E1%84%8E%E1%85%A5%E1%86%AB,%20%E1%84%8B%E1%85%B2%E1%84%89%E1%85%A1%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8C%E1%85%A6%E1%84%80%E1%85%A9%E1%86%BC%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%20%E1%84%80%E1%85%AE%E1%84%8E%E1%85%AE%E1%86%A8%202fbcf4f31dea42929748ab794be872aa/Untitled%204.png)
    
    ![Untitled](%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8B%E1%85%AD%E1%84%8B%E1%85%A3%E1%86%A8,%20%E1%84%8E%E1%85%AE%E1%84%8E%E1%85%A5%E1%86%AB,%20%E1%84%8B%E1%85%B2%E1%84%89%E1%85%A1%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8C%E1%85%A6%E1%84%80%E1%85%A9%E1%86%BC%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%20%E1%84%80%E1%85%AE%E1%84%8E%E1%85%AE%E1%86%A8%202fbcf4f31dea42929748ab794be872aa/Untitled%205.png)
    
- 평가 기준
- 배경
    - 제품을 살 때, 유튜브와 구글에 쏟는 시간이 너무 많고 텍스트화 하는 작업이 너무 불편하다
    - 텍스트화를 왜 하느냐 비슷한 제품을 찾고 그 제품에 대한 특성을 비교해서 아는 것이 중요하기 때문
    - 유튜브를 왜 보는가? 그 제품에 대한 나보다 전문가인 공인이 쉽게 설명하기에 그렇다.
- 이대로 괜찮은가 보충 아이디어 설명 → 방향성 설정에 대한 (제품 판매)
    - 키워드 입력방식 2가지
        - 카테고리, 특성 →
            - 특정 아이템에 대한 필요한 특징을 알아온다.(예. 자동차 → 색, 가격, 후륜, 전륜 등..)
            - 특성과 카테고리에 맞는 몇가지 아이템에 대한 설명 특성 가져오기
                - 특정 사이트에서 특정 아이템에 대한 정보 가져오기 예) 다나와 제품 정보 및 제품명
                - 유튜브에서 제품명에 대한 검색 후 유튜버의 정보 소개 내용 요약 전달.
                - 제공받은 특성에 맞는 제품 추천
        - 카테고리, 제품명
            - 제품명에 대한 특징을 가져오기
            - 제공 받은 제품명과 관련된 특징을 가진 다른 제품 추천하기
            - 유튜브에서 제품명에 대한 검색 후 유튜버의 정보 소개 내용 요약 전달.
            - 제공받은 특성에 맞는 또 다른 제품 추천
        - 기대효과
            - 특정 제품에 대한 대중 평가 정보와 스펙에 대한 정보 및 추천 제품을 한번에 알 수 있음.
- 기능적인거 추가 할 수 있는거 뭐가 있을 지
- 구현 방식
- 키워드를 입력하면 핵심 내용(단어) 파악후 그에 대한 정리보여주기(백과사전 형식으로-위키백과 느낌으로, 사용자가 추가 가능) 그리고 이와 비슷한 그룹에 속한것과, 상위 그룹, 하위 그룹으로 갈 수 있는 링크 제공(상위로 갈수록 포괄적인 대중적인 지식 파악 가능(상식)- 하위로 갈수록 지엽적인 전문적인 지식 습득 가능
- 기존의 있었던 기술   : 참신성
- 어떤 정보를 어떤 지표로

- 총정리
    - 현 상태 유지는 괜찮다.
    - 준비사항
        - 데이터 → 즉, 추천을 하기 위해 어떤 데이터를 사용할 것인가?
        - 알고리즘 → 어떤 지표를 활용해 어떤 모델을 구축할 것인가?
        - 영상 추천, 제품추천임. 해당 제품과 비슷한 특징을 가진 다른 제품을 추천하는데 여기에 영상적인 지표가 추가되는거임.
        - 영상지표로 사용할 영상은 어떤 기준으로 뽑을 것이며, 
        뽑은 영상들 중에서 어떤 기준으로
        - 요약을 어떻게 빠르게 할지..
        - 영상에서 제품에 대한 것을 긍정 몇 퍼센트 부정 몇 퍼센트 수치화하는 것
        - 해외 유저들의 반응도 얻을 수 있음.
        

## 아이디어 픽스

- 입력: 제품명
    - 명확한 제품명이 아닌 제품 이름에 해당 단어가 포함되어 있으면 됨
        
        예시) **나이키 에어포스 → 이 단어가 포함된 제품들을 찾아라**
        
    - 보완점(부가적으로 구현할 부분)
        - 입력방식 추가 : 신발 이미지
- 입력에 대한 출력 : 입력에 해당하는 제품 1개
    
    **긍부정비율**, **리뷰개수순위 → 두지표를 고려해서 제품 하나만 뽑기**
    
    - 제품 요약:
        - 다나와 정보 제공
            - 제품명,
            - 제품사진,
            - 색상,
            - 종류,  → 종류 구체화(몇 가지로 할 것인가 ex. 구두, 운동화, 슬리퍼 등 최대한 다나와에 있는 종류대로 저장하는 것이 좋음)
            - 소재,
            - 리뷰개수
        - 영상적 정보 제공
            - 긍부정 비율(중요) : 감성평가에 대한 자연어 처리 알고리즘 모색
            - 스타일링 제안
            - 사이즈
            - 제품특징
            - 신뢰도 평가 →(광고, 등등…) 추후
    - 제품 추천:
        - 이미지유사도 & 특성 유사도 판별 후 랭킹 매겨서 20개만 뽑기
            - 너무 비슷한 제품군(색깔만 다르거나, 년도만 다르거나)이면 1개만 뽑기
        - 추천 후 마지막에 긍부정지표로 랭킹 메겨서 4순위까지만 보여주기
        - 사용자 입력을 추가로 받는 부분 (일단 구현 후 추가 예정)
            - 예시 ) 추천된 제품 중 사용자가 더 가격이 싼 제품군을 원할때

- 머신러닝 또는 딥러닝 으로 사진 유사도를 추출 정보 활용 법
    - 모든 특징들을 다 고려해서 유사도를 찾기.
- 어떤점에서 기존의 시스템과 다른가?
    - 영상적 지표 활용
    - 리뷰활용도 가능(긍부정 비율에 넣기)
- 같은 제품군들끼리 묶어놓아야하는 이유는?
    - ??
- 영상적 지표에서 더 활용가능한 정보(진행하면서 추가할 예정)
    - 댓글 수 및 긍정부정댓글
    - 광고성 여부
    - 싫어요, 좋아요 수
    - 구독자 수
- 이미지 유사도 인식
    - [https://mapadubak.tistory.com/121](https://mapadubak.tistory.com/121) (신발 이미지 유사도 프로젝트)
        - [https://ichi.pro/ko/python-eul-sayonghayeo-imiji-geomsaeg-enjin-guchug-190319101887515](https://ichi.pro/ko/python-eul-sayonghayeo-imiji-geomsaeg-enjin-guchug-190319101887515) (위의 프로젝트에서 활용한 기본코드)
    - [https://github.com/devnjw/ShoeSearch](https://github.com/devnjw/ShoeSearch) (이미지 입력으로 비슷한 신발을 찾아내는 프로젝트
- gpt 프롬프트 다루기
    
    [https://www.gpters.org/c/ai-developers/a-gpt-3-5-16k-api-pdf](https://www.gpters.org/c/ai-developers/a-gpt-3-5-16k-api-pdf)
    

## 보고서 및 ppt회의

- 배경설명, 문제정의,
- 소개 및 차별성,
- 해결방안제시,
- 시스템 아키텍처,
- 다이어그램,
- 유아이유엑스(웹),
- 주요기능설명,
- 핵심코드설명(한장으로 바로 알 수 있도록 핵심 부분 주석 달면서 명확하게)
- 향후계획,  시행착오

발표는 자연스럽게하기. 연결적인 흐름이 자연스럽게

아이디어가 명확하지 않다보니 지루해짐.
이유 : 이미 잔뜩 있는 기능들을 발전시키기 어려움.

에비던스 보여주기.
시스템개요 무조건.

구체적인 예시
설문조사 - 제품 비교 앱.

![Untitled](%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8B%E1%85%AD%E1%84%8B%E1%85%A3%E1%86%A8,%20%E1%84%8E%E1%85%AE%E1%84%8E%E1%85%A5%E1%86%AB,%20%E1%84%8B%E1%85%B2%E1%84%89%E1%85%A1%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8C%E1%85%A6%E1%84%80%E1%85%A9%E1%86%BC%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%20%E1%84%80%E1%85%AE%E1%84%8E%E1%85%AE%E1%86%A8%202fbcf4f31dea42929748ab794be872aa/Untitled%206.png)

![Untitled](%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8B%E1%85%AD%E1%84%8B%E1%85%A3%E1%86%A8,%20%E1%84%8E%E1%85%AE%E1%84%8E%E1%85%A5%E1%86%AB,%20%E1%84%8B%E1%85%B2%E1%84%89%E1%85%A1%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8C%E1%85%A6%E1%84%80%E1%85%A9%E1%86%BC%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%20%E1%84%80%E1%85%AE%E1%84%8E%E1%85%AE%E1%86%A8%202fbcf4f31dea42929748ab794be872aa/Untitled%207.png)

웹 사이트에 접속합니다. 이때 사용자의 요청은 **Nginx 웹 서버**로 전달됩니다. Nginx는 정적 파일에 대한 요청을 바로 응답하거나, 동적 콘텐츠에 대한 요청을 **Gunicorn**으로 전달합니다.

Gunicorn은 요청을 받으면 이를 **Flask 웹 애플리케이션**에 전달합니다. Flask는 요청을 처리하기 위해 필요한 로직을 실행하고, 외부 서비스인 **Google Trends**나 **YouTube Data API v3**에서 데이터를 가져온 후 앞서 설명했던 방식으로 추천과 요약을 진행합니다. 그리고 이에 관한 것들을 **MySQL 데이터베이스**에서 정보를 조회하거나 저장합니다.

처리가 완료된 후, Flask는 결과를 Gunicorn에게 반환하고, Gunicorn은 이를 다시 Nginx에게 전달합니다. 마지막으로, Nginx는 처리된 결과를 사용자의 브라우저에게 보내줍니다.

이 모든 시스템은 **AWS Lightsail**에서 호스팅되며, 안정적인 인터넷 연결과 리소스를 제공받아 운영됩니다.

→ 다듬어야함.

보고서에 들어가야 할 내용

서론

- 배경 설명, 사례분석
    
    많은 사람들이 제품을 구매할 때 다양한 정보 소스를 활용한다. 특히 요즘에는 두 가지 경로 온라인 쇼핑몰 사이트와 유튜브 영상으로 정보를 얻는다. 이들 경로를 통해 소비자들은 제품에 대한 자세한 정보, 사용 후기, 평가 등을 얻을 수 있으며 이러한 정보는 구매 결정 과정에서 중요한 역할을 하고있다.
    
    이러한 정보들은 때때로 제품 사용 시 발생할 수 있는 불편함이나 문제점에 대해 충분히 설명하지 않을 수 있으며 또한 잘못된 정보와 리뷰의 신뢰성등의 문제로 소비자들은 리뷰와 평가를 비판적으로 분석하고, **가능하다면 다양한 소스에서 정보를 수집하여 종합적인 평가를 하는 것이 중요해지고 있다. (여기에 피피티때 사용했던 사진들 삽입해도 좋을듯)**
    
    문제점 : 
    
    제품에 대한 선택적 정보 제공 , 과장된 정보, 리뷰 조작, 광고성, 복잡성, 혼란
    
- 문제 정의
    
    제품을 구매할 때, 다양한 소스에서 정보를 수집하는 것이 불가피 하지만 다양한 온라인 사이트를 방문하며 정보를 수집하는 과정에서 불필요한 복잡성과 혼란을 겪고 있으며 각 사이트마다 제공되는 정보의 양과 품질이 상이하다, 이로 인해 어떤 정보가 신뢰할만하고 어떤 것이 그렇지 않은지를 판단하는 데 어려움을 겪고 있다.
    
    또한, 각 사이트는 긍정적인 리뷰를 강조하려는 경향이 있어 과장된 정보나 편향된 의견을 식별하는 것이 힘들어지고 있다. 이로 인해 소비자로서 정확하고 신뢰할만한 정보를 얻기 위해서는 더 많은 노력과 시간을 투자해야 하는 상황이다.
    
    좀 더 나은 정보를 찾기 위해 어떤 사이트를 신뢰할 수 있는지, 어떤 평가 기준을 활용해야 하는지에 대한 명확한 지침이 부족하면서, 이로 인해 제품 선택에 대한 불안이 더해지고 있다. 
    
- 극복 방안
    
    이러한 어려움을 극복하고자 제품에 대한 정보를 탐색할 수 있는 여러 사이트들을 통해서 정보를 취합해 소비자들의 불필요한 복잡성과 혼란을 겪지 않을 수 있는 제품에 대해 신뢰할 수 있는 정확한 정보 제공해주는 서비스를 만들어보자고 생각을 했다. 
    

본론

- 시스템 개요 - 구체적 그림, 표 등의 시각 자료
- 필요한 기술 요소 설명
- 구현 방법 및 개발 방향

결론

- 서비스의 강점 :
    - 요약 → 사이즈추천, 제품고유특징, 스타일링제안, 제품고유 키워드,  추천도, 추천상품
        - 소재 → 유사도
        - 카테고리 → 유사도
        - 이미지 → 유사도
        - 핵심키워드적 → 유사도
        - 어쩔 수 없는게 단어적유사도만. 형태소적 (글자자체적 유사도)
        - 도메인전문가가 딸려와야한다.
    - 유튜브. → 어느정도 카테고리적 정보에 지식이 있는 사람들이라 정보의 신뢰성이 높고 꿀정보.
    - 여러 판매 사이트. 정보
    - 다양한 카테고리
    - 정보를 하나를 통해 뽑아내는 것이 아닌 20개, 100개, 공통된 내용을 뽑아내기 떄문에 신뢰성이 높다.
    - 블랙프라이데이. → 급급하다.
    - 얘기를 할 때 좀 더 개인화, 가 아닌 대중화적으로 말하기. 세뇌하듯이 너도 그랬잖아.
        - 제품을 사고 마음에 안들었던 경험은 충분히 있다.
    

## 제품 설명

csv에 저장된 정보 → db에 저장되어 있다고 말하면 됨.

- 제품명,
- 카테고리, - 유사도 측정 지표1(단어유사도)
- 주소재, - 유사도 측정 지표2(단어유사도)
- 리뷰 수, - 추천도 측정 지표1
- 이미지url, - 유사도 측정 지표3(이미지유사도)
- 리뷰별점, - 추천도 측정 지표2
- 리뷰 내용 - 추천도 지표3(감성평가)

—————위는 크롤링한 정보—————

——아래 유튜브 api로 제품 리뷰영상을 가져와 gpt로 다듬은 정보———

- 사이즈 추천 - 요약데이터
- 스타일링제안 - 요약데이터
- 제품 고유 특징 - 요약데이터
- 제품 주요 키워드 - 유사도 측정 지표4(단어유사도)
- 제품 설명 - 추천도 측정 지표4(감성평가)

전체적인 플로우

1. 크롤링을 통해 제품의 정보를 가져온다.
    - 제품명
    - 카테고리
    - 주소재
    - 리뷰수
    - 이미지 url
    - 리뷰별점
    - 리뷰내용
2. youtube api를 통해 제품명에 해당되는 영상에서 자막 데이터를 가져온다.
3. 자막 데이터를 바탕으로 다음 정보를 gpt api를 통해 추출한다.
    - 사이즈 추천
    - 스타일링 제안
    - 제품 고유 특징
    - 제품 주요 키워드
    - 제품관련 설명
4. 리뷰내용과 제품관련 설명을 감성평가를 진행한다.
5. 리뷰 수, 리뷰별점과 감성평가를 마친 리뷰내용, 감성평가를 마친 제품 관련 설명을 바탕으로 추천도를 측정한다.
6. 이미지, 소재, 카테고리, 제품 주요 키워드적 유사도를 총체적으로 각각 다른 가중치로 측정하여 유사한 제품을 뽑아낸다. (현재는 형태소적인 유사도만 측정한다.)
    
    
7. 입력 제품에 대해 같은 이름을 가진 제품은 리뷰수와 추천도를 바탕으로 가장 상위 제품을 출력
8. 유사 제품에 대해서는 약 30개 제품에 대해 유사도를 뽑은 후 추천도로 다시 정렬 후 3제품을 출력.

전체적인 플로우는 위와 같고 세세한 기술 설명

코드 : 

[youtube_data_api.ipynb](%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8B%E1%85%AD%E1%84%8B%E1%85%A3%E1%86%A8,%20%E1%84%8E%E1%85%AE%E1%84%8E%E1%85%A5%E1%86%AB,%20%E1%84%8B%E1%85%B2%E1%84%89%E1%85%A1%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8C%E1%85%A6%E1%84%80%E1%85%A9%E1%86%BC%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%20%E1%84%80%E1%85%AE%E1%84%8E%E1%85%AE%E1%86%A8%202fbcf4f31dea42929748ab794be872aa/youtube_data_api.ipynb)

1. 추천도 계산
    - 감성분석 :
        
        감성 분석 점수 : 리뷰 감성 분석은 hugging face의
        `jaehyeong/koelectra-base-v3-generalized-sentiment-analysis` 
        감성분석으로 파인튜닝된 모델 사용. 
        
        문장을 입력으로 넣고 라벨(0부정과 1긍정)과 라벨에 대한 확률이 출력으로 나옴.
        
        예시: 
        
        ![Untitled](%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8B%E1%85%AD%E1%84%8B%E1%85%A3%E1%86%A8,%20%E1%84%8E%E1%85%AE%E1%84%8E%E1%85%A5%E1%86%AB,%20%E1%84%8B%E1%85%B2%E1%84%89%E1%85%A1%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8C%E1%85%A6%E1%84%80%E1%85%A9%E1%86%BC%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%20%E1%84%80%E1%85%AE%E1%84%8E%E1%85%AE%E1%86%A8%202fbcf4f31dea42929748ab794be872aa/Untitled%208.png)
        
        긍정리뷰의 경우 그대로 점수를 사용, 부정리뷰의 경우 1-score(확률점수)사용
        
        이러한 점수들의 평균을 구하여 review_score를 결정
        
    - 리뷰 개수 점수
        
        제품에 대한 리뷰의 개수를 바탕으로 함.
        
        리뷰 개수에 로그 스케일을 적용하여 많은 리뷰를 가진 제품이 높은 점수를 받지만 리뷰 개수의 증가에 따른 점수 상승률은 점점 감소토록 설정함. 최대 1까지 가능.
        
    - 리뷰 평점 점수
        
        이 점수는 제품의 평균 평점(별점)을 사용
        
        평점은 5점 만점으로 설정하였으며, 이를 0과 1사이의 값으로 정규화하여 계산함.
        
    - 최종적으로 이 세가지 점수에 가중치(weights)를 적용하여 종합 추천 지표를 계산해 내고 이 값이 높을 수록 제품이 더 추천할 만하다는 것을 의미함. 0~1사이의 값을 가지게 됨.
    - 추후 개선점 :
        1. 유저 피드백을 통한 가중치의 적절한 설정(지금은 임의의 값임)
        2. 유튜브 리뷰 영상 → 음성적인 지표 또한 고려
        3. 좀 더 다양한 사이트에서 리뷰를 가져오기
    - 코드
        
        ```python
        # 모델 및 토크나이저 로드
        tokenizer = AutoTokenizer.from_pretrained("jaehyeong/koelectra-base-v3-generalized-sentiment-analysis")
        model = AutoModelForSequenceClassification.from_pretrained("jaehyeong/koelectra-base-v3-generalized-sentiment-analysis")
        sentiment_classifier = TextClassificationPipeline(tokenizer=tokenizer, model=model)
        
        sentences = split_text_to_sentences(video_summaries_sentiment)
                sentiment_results = []
        
                for review in sentences:
                    try:
                        # 토큰 길이 확인
                        tokens = tokenizer.encode(review, truncation=False, add_special_tokens=False)
                        if len(tokens) > 512:
                            continue
        
                        pred = sentiment_classifier(review)
                        sentiment_results.append({
                            'label': pred[0]['label'],
                            'score': pred[0]['score']
                        })
                    except RuntimeError as e:
                        continue
                weights = {'review_score': 0.4, 'review_count_score': 0.3, 'review_rating': 0.3}
                # 감성 분석 결과를 바탕으로 review_score 계산
                if sentiment_results:
                    scores = [result['score'] for result in sentiment_results]
                    labels = [1 if result['label'] == 'LABEL_1' else 0 for result in sentiment_results]
                    review_score = sum(score if label == 1 else 1 - score for score, label in zip(scores, labels)) / len(sentiment_results)
                else:
                    review_score = 0
        
                # 리뷰 수에 대한 점수 계산
                review_count = row['review_num']
                review_count_score = min(1, (np.log(review_count + 1) / np.log(100 + 1)))
        
                # 리뷰 평점 점수 계산
                review_rating = row['rating']
                review_rating_score = review_rating / 5  # 평점을 0과 1 사이의 값으로 정규화
        
                # 종합 추천 지표 계산
                recommendation_score = (
                    review_score * weights['review_score'] +
                    review_count_score * weights['review_count_score'] +
                    review_rating_score * weights['review_rating']
                )
        ```
        
2. 유사 제품 추천
    - 이미지 유사도
        
        VGG16은 기본적으로 Classification을 위한 모델이고, imagenet도 1000개의 label이 있는 image classification dataset이다. 하지만 결국 CNN이 하는 일은 각 이미지의 Feature를 Extract하는 것임.
        
        Extract한 Feature를 가지고 Softmax를 하면 가장 일치하는 Label을 찾을 수 있는 것인데, Softmax를 안하고 Fully Connected Layer까지만 통과하면 Feature Vector가 나온다.
        
        FC Layer를 통과했을 때 output을 뽑아서 저장하면 되는 것임.
        
        다시 정리하자면
        
        VGG-16 모델을 사용하여 이미지의 특징을 추출하고 VGG-16은 이미지 분류에 널리 사용되는 딥러닝 모델로, ImageNet 데이터셋으로 사전 학습된 가중치를 사용하여 주어진 이미지로부터 특징을 추출하여 정규화된 형태로 반환한다.
        
        데이터베이스에 저장된 신발 사진들의 Feature를 모두 뽑아서 저장하고, 사용자가 신발명을 입력하면 그 신발의 feature과 유사한 다른 신발의 feature를 찾아서 정렬한다.
        
        그리고 그 값은 distance형태로 표현되며 0~1사이의 값을 가지고 값이 적을수록 유사한 제품이다.
        
        - 코드
            
            ```python
            from tensorflow.keras.preprocessing import image
            from tensorflow.keras.applications.vgg16 import VGG16, preprocess_input
            from tensorflow.keras.models import Model
            import numpy as np
            import os
            
            class FeatureExtractor:
                def __init__(self):
                    # VGG-16 모델을 사용하고, 가중치는 ImageNet에서 사전 학습된 것을 사용
                    base_model = VGG16(weights='imagenet')
                    # 모델을 커스터마이즈하여 완전연결층(fc1)에서 특징을 반환하도록 설정.
                    self.model = Model(inputs=base_model.input, outputs=base_model.get_layer('fc1').output)
            
                def extract(self, img):
                    # 이미지 크기를 조정합니다. VGG-16의 표준 입력 크기인 224x224로 설정
                    img = img.resize((224, 224))
                    # 이미지의 색공간을 RGB로 변환
                    img = img.convert('RGB')
                    # 이미지를 배열로 변환하고, 형식을 전처리
                    x = image.img_to_array(img)
                    x = np.expand_dims(x, axis=0)
                    x = preprocess_input(x)
                    # 이미지에서 특징을 추출
                    feature = self.model.predict(x)[0]
                    # 추출된 특징의 L2 노름으로 정규화하여 반환
                    return feature / np.linalg.norm(feature)
            ```
            
    - 소재 유사도
        
        미리 비슷한 소재들에 대해 유사성을 판단하여 그 특성을 고려하기 위해 벡터형태로 나타낸다.
        
        - 내구성
        - 방수성
        - 유연성
        - 무게
        - 질감
        - 통기성
        
        각 특성을 0~1사이의 값으로 정규화를 한 후 두 제품 벡터간의 코사인유사도를 계산하여 소재 간 유사도를 계산한다.
        
        - 하지만 지금은 도메인 지식의 부족으로 인해 단순 단어적 유사도(형태소적 유사도)만 고려했다
    - 카테고리 유사도
        
        미리 비슷한 카테고리들에 대해 유사성을 판단하여 그 특성을 고려하기 위해 벡터형태로 나타낸다.
        
        - 운동화
        - 샌들
        - 구두
        - 나막신
        - 하이힐
        - 부츠
        
        카테고리를 완벽하게 분류하며 비슷한 카테고리의 관계에 대한 것을 수치화할 수 있는 도메인적 지식이 필요함.
        
    - 키워드적 유사도
        
        gpt api 프롬프트 엔지니어링을 통한 제품 고유특징에 대하여 각 리뷰영상에서 추출한 후
        
        각 리뷰영상에서의 공통 키워드를 다시 추출한다.
        
        그 후 단어적 유사도를 판별하여 0~1의 수치로 표현한다.
        
    - 결론적으로
        - 이미지로 유사도를 정렬한 후 상위 10개에서 추천도를 기준으로 다시 정렬하여 가장 상위 제품을 하나 출력
        - 소재, 카테고리적 유사도로 정렬한 후 상위 10개에서 추천도를 기준으로 다시 정렬하여 가장 사위 제품을 하나 출력
        - 키워드적 유사도를 기준으로 정렬한 후 상위 10개에서 추천도를 기준으로 다시 정렬하여 가장 상위 제품을 하나 출력
        - 총체적 유사도를 기반으로 정렬한 후 상위 10개에서 추천도를 기준으로 다시 정렬하여 가장 상위 제품을 하나 출력
3. 요약 추출
    - youtube data api v3를 통해 입력제품 리뷰영상 id를 가져옴.
        
        ```python
        import pandas as pd
        from googleapiclient.discovery import build
        import json
        
        def youtube_search(shoe_name, api_key):
            api_service_name = "youtube"
            api_version = "v3"
            api_key = api_key
        
            youtube = build(api_service_name, api_version, developerKey=api_key)
        
            request = youtube.search().list(
                part="snippet",
                regionCode='KR',
                q=shoe_name,
                maxResults=10,
                type="video",
                order='relevance'
            )
            response = request.execute()
            with open('response.json', 'w') as outfile:
                json.dump(response, outfile, indent=4)
                    
            # 응답을 JSON 파일로 저장
        def get_videos_with_captions(shoe_name, api_key):
            youtube = build("youtube", "v3", developerKey=api_key)
        
            # 검색어에 대한 동영상 20개 검색
            search_response = youtube.search().list(
                part="snippet",
                q=shoe_name,
                maxResults=20,
                type="video"
            ).execute()
        
            videos_with_captions = []
            for item in search_response.get("items", []):
                video_id = item["id"]["videoId"]
        
                # 각 동영상에 대해 자막 존재 여부 확인
                captions_response = youtube.captions().list(
                    part="snippet",
                    videoId=video_id
                ).execute()
        
                if captions_response["items"]:
                    videos_with_captions.append(video_id)
        
                # 최대 10개 동영상만 저장
                if len(videos_with_captions) >= 10:
                    break
        
            return videos_with_captions
        
        from googleapiclient.discovery import build
        
        def get_videos_for_query(query, api_key):
            youtube = build("youtube", "v3", developerKey=api_key)
        
            # 검색어에 대한 동영상 20개 검색 (ID만 가져오기)
            search_response = youtube.search().list(
                part="id",
                q=query,
                maxResults=20,
                type="video"
            ).execute()
        
            # 검색 결과로부터 비디오 ID 추출
            video_ids = [item["id"]["videoId"] for item in search_response.get("items", [])]
        
            return video_ids
        ```
        
    - youtube_transcript_api를 통해 영상에 대한 자막 데이터를 가져옴.
        
        ```python
        def extract_transcripts_id(videos_with_captions):
            transcripts = {}
            long_transcripts = {}
            short_transcripts = {}
            
            for video_id in videos_with_captions:
                try:
                    transcript_list = YouTubeTranscriptApi.get_transcript(video_id, languages=['ko', 'en'])
                    texts = [entry['text'] for entry in transcript_list if not re.search(r'\[.*?\]', entry['text'])]
                    combined_text = ' '.join(texts)
        
                    # 200자 이상과 미만을 구분하여 저장
                    if len(combined_text) >= 200:
                        long_transcripts[video_id] = combined_text
                    else:
                        short_transcripts[video_id] = combined_text
        
                except Exception as e:
                    print(f"No transcript available for video ID {video_id}: {e}")
        
            # 영상 수가 10개 이상인 경우, 200자 이상의 자막만 우선 선택
            if len(videos_with_captions) >= 10:
                for video_id, transcript in long_transcripts.items():
                    transcripts[video_id] = transcript
                    if len(transcripts) >= 10:
                        return transcripts
            
            # 200자 이상의 자막이 5개 미만인 경우, 200자 미만의 자막도 포함
            for video_id, transcript in short_transcripts.items():
                if video_id not in transcripts:
                    transcripts[video_id] = transcript
                    if len(transcripts) >= 10:
                        break
        
            return transcripts
        ```
        
    - 각 영상의 자막 데이터에서 gpt api를 통해 세가지 지표에 대한 정보를 뽑아옴
        - 사이즈 추천
        - 스타일링 제안
        - 제품 고유 특징
        
        ```python
        import json
        import openai
        import re
        
        def get_summary(text, shoe_name):
            openai.api_key = "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"
        
            prompt = f"입력된 영상 텍스트에서 {shoe_name}에 관한 내용만 아래 세가지 사항의 정보를 개조식으로 보여주고 개조식에 해당되는 내용을 제외한 다른 정보는 말하지마.\n 언급이 되지 않은 정보라면 빈칸으로 냅둬\n - 사이즈 추천(큰 사이즈, 정사이즈, 작은 사이즈 특정 사이즈에 대한 언급은 하지마) : \n - 스타일링 제안 :\n - 제품 고유 특징({shoe_name}에 관해 언급된 내용만 적어줘. 다른 제품에 대해 적은 내용을 답변하면 안돼.) : "
            response = openai.ChatCompletion.create(
                model="gpt-3.5-turbo-16k",
                timeout = 600,
                messages=[
                    {"role": "system", "content": prompt},
                    {"role": "user", "content": text}
                ]
            )
            return response['choices'][0]['message']['content']
        
        def split_text_to_fit_token_limit(text, token_limit=2000):
            sentences = re.split(r'(?<!\w\.\w.)(?<![A-Z][a-z]\.)(?<=\.|\?)\s', text)
            current_text = ""
            texts = []
        
            for sentence in sentences:
                potential_text = f"{current_text} {sentence}".strip()
                if len(potential_text) > token_limit:
                    texts.append(current_text.strip())
                    current_text = sentence
                else:
                    current_text = potential_text
        
            if current_text:
                texts.append(current_text.strip())
            return texts
        
        import re
        def parse_examples(text):
            # 각 예시를 구분하여 리스트화
            examples = re.split("\n", text)
            examples = [item for item in examples if item != ""]
            
            try:
                # 각 예시를 딕셔너리로 변환
                example_dict = {
                    "size_recommendation": examples[0].split(": ")[1],
                    "styling_suggestion": examples[1].split(": ")[1],
                    "unique_product_features": examples[2].split(": ")[1]
                }
            except IndexError:
                return None  # 인덱스 오류 발생 시 None 반환
        
            return example_dict
        
        def summarize_transcripts(transcripts_data, product_name):
            full_summary = {}
        
            for video_id, transcript_text in transcripts_data.items():
                splitted_texts = split_text_to_fit_token_limit(transcript_text)
                for text in splitted_texts:
                    summary = get_summary(text, product_name)
                    parsed_summary = parse_examples(summary)
        
                    if parsed_summary is not None:
                        full_summary[video_id] = parsed_summary
        
            return full_summary
        ```
        
    - 각 영상의 세가지 지표에 대해 공통 내용에 대해 각 특징 총체적 취합 내용 추출
        
        ```python
        def collect_features(video_summaries):
            """각 비디오별 세 가지 특징을 각각의 리스트로 취합합니다."""
            size_recommendations = []
            styling_suggestions = []
            unique_product_features = []
        
            for video_id, features in video_summaries.items():
                if 'size_recommendation' in features:
                    size_recommendations.append(features['size_recommendation'])
                if 'styling_suggestion' in features:
                    styling_suggestions.append(features['styling_suggestion'])
                if 'unique_product_features' in features:
                    unique_product_features.append(features['unique_product_features'])
        
            return size_recommendations, styling_suggestions, unique_product_features
        
        def get_combined_summary(texts, feature, shoe_name):
            openai.api_key = "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"
            text_combined = ' '.join(texts)
            prompt = f"해당 text는 {shoe_name}에 대한 {feature}사항의 정보야.\n한국어로 답변하고 공통된 내용을 다섯줄로 한 개조식이 아닌 형태로 요약해줘. 언급되지 않았다는 내용은 답변하지 마.\n 해당 내용을 제외한 다른 답변은 절대로 말하지 마!.\n\n - {feature} : "
            response = openai.ChatCompletion.create(
                model="gpt-3.5-turbo-16k",
                messages=[
                    {"role": "system", "content": prompt},
                    {"role": "user", "content": text_combined}
                ]
            )
            # GPT-3 응답을 문자열로 처리
            response_text = response['choices'][0]['message']['content']
        
            # 응답을 문장 단위로 분리
            sentences = response_text.split('. ')
        
            # 필터링 조건에 따라 문장을 선택
            filtered_sentences = []
            for sentence in sentences:
                if '언급' in sentence and '않' in sentence:
                    continue
                filtered_sentences.append(sentence)
        
            # 필터링된 문장을 하나의 문자열로 결합
            return ' '.join(filtered_sentences)
        
        def combine_summaries(size_recommendations, styling_suggestions, unique_product_features, shoe_name):
            size_combined_summary = get_combined_summary(size_recommendations, "size_recommendations", shoe_name)
            styling_combined_summary = get_combined_summary(styling_suggestions, "styling_suggestion", shoe_name)
            feature_combined_summary = get_combined_summary(unique_product_features, "unique_product_features", shoe_name)
        
            return {
                'size_recommendations': size_combined_summary,
                'styling_suggestion': styling_combined_summary,
                'unique_product_features': feature_combined_summary
            }
        ```
        
    
    ```markup
    total 요약 결과물
    {'size_recommendations': '팀버랜드 6인치 부츠는 일반적인 신발 사이즈와 동일한 사이즈를 선택하는 것이 좋으며, 발볼이 넓은 분들은 반 사이즈 업하는 것을 추천합니다. 발이 작은 분들은 정사이즈를 고려해보세요. 개인의 발볼과 발등의 높이에 따라 사이즈를 조절할 수 있으므로, 착용하기 전에 직접 신어보고 편안한 사이즈를 선택하는 것이 좋습니다.',
     'styling_suggestion': '팀버랜드 6인치는 다양한 스타일링에 활용할 수 있는 클래식하고 세련된 부츠이다. 청바지나 스키니진과의 조합으로는 캐주얼한 룩에 어울리며, 와이드한 바지와 매치하면 스트릿 스타일로 연출할 수 있다. 블랙 와이드 팬츠와 함께 하면 고급스러운 분위기가, 수에 팬츠와 함께 하면 자연스럽고 편안한 느낌을 줄 수 있다. 또한, 테일러드 슬랙스나 조거 팬츠와의 조합으로는 캐주얼한 비즈니스 스타일로도 연출할 수 있다.',
     'unique_product_features': '팀버랜드 6인치 부츠는 완벽한 방수 기능과 내구성, 효율적인 보온성을 제공한다. 슬림한 실루엣과 스타일적인 매력도 특징이다. 편안한 착용감과 신축성도 견고한 환경에서도 유지된다. 스웨이드 소재로 제작되며, 생활방수 기능도 갖추고 있다. 디자인은 간결하고 무겁지 않은 특징을 가지고 있다.'}
    ```
    

## PPT에 넣을 자료

1. 요약
    
    ![Untitled](%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8B%E1%85%AD%E1%84%8B%E1%85%A3%E1%86%A8,%20%E1%84%8E%E1%85%AE%E1%84%8E%E1%85%A5%E1%86%AB,%20%E1%84%8B%E1%85%B2%E1%84%89%E1%85%A1%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8C%E1%85%A6%E1%84%80%E1%85%A9%E1%86%BC%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%20%E1%84%80%E1%85%AE%E1%84%8E%E1%85%AE%E1%86%A8%202fbcf4f31dea42929748ab794be872aa/Untitled%209.png)
    
    ![Untitled](%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8B%E1%85%AD%E1%84%8B%E1%85%A3%E1%86%A8,%20%E1%84%8E%E1%85%AE%E1%84%8E%E1%85%A5%E1%86%AB,%20%E1%84%8B%E1%85%B2%E1%84%89%E1%85%A1%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8C%E1%85%A6%E1%84%80%E1%85%A9%E1%86%BC%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%20%E1%84%80%E1%85%AE%E1%84%8E%E1%85%AE%E1%86%A8%202fbcf4f31dea42929748ab794be872aa/Untitled%2010.png)
    
    ![Untitled](%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8B%E1%85%AD%E1%84%8B%E1%85%A3%E1%86%A8,%20%E1%84%8E%E1%85%AE%E1%84%8E%E1%85%A5%E1%86%AB,%20%E1%84%8B%E1%85%B2%E1%84%89%E1%85%A1%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8C%E1%85%A6%E1%84%80%E1%85%A9%E1%86%BC%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%20%E1%84%80%E1%85%AE%E1%84%8E%E1%85%AE%E1%86%A8%202fbcf4f31dea42929748ab794be872aa/Untitled%2011.png)
    
    ![Untitled](%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8B%E1%85%AD%E1%84%8B%E1%85%A3%E1%86%A8,%20%E1%84%8E%E1%85%AE%E1%84%8E%E1%85%A5%E1%86%AB,%20%E1%84%8B%E1%85%B2%E1%84%89%E1%85%A1%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8C%E1%85%A6%E1%84%80%E1%85%A9%E1%86%BC%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%20%E1%84%80%E1%85%AE%E1%84%8E%E1%85%AE%E1%86%A8%202fbcf4f31dea42929748ab794be872aa/Untitled%2012.png)
    
2. 추천
    
    ![Untitled](%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8B%E1%85%AD%E1%84%8B%E1%85%A3%E1%86%A8,%20%E1%84%8E%E1%85%AE%E1%84%8E%E1%85%A5%E1%86%AB,%20%E1%84%8B%E1%85%B2%E1%84%89%E1%85%A1%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8C%E1%85%A6%E1%84%80%E1%85%A9%E1%86%BC%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%20%E1%84%80%E1%85%AE%E1%84%8E%E1%85%AE%E1%86%A8%202fbcf4f31dea42929748ab794be872aa/Untitled%2013.png)
    
    ![Untitled](%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8B%E1%85%AD%E1%84%8B%E1%85%A3%E1%86%A8,%20%E1%84%8E%E1%85%AE%E1%84%8E%E1%85%A5%E1%86%AB,%20%E1%84%8B%E1%85%B2%E1%84%89%E1%85%A1%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8C%E1%85%A6%E1%84%80%E1%85%A9%E1%86%BC%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%20%E1%84%80%E1%85%AE%E1%84%8E%E1%85%AE%E1%86%A8%202fbcf4f31dea42929748ab794be872aa/Untitled%2014.png)
    
3. 유사도
    
    ![Untitled](%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8B%E1%85%AD%E1%84%8B%E1%85%A3%E1%86%A8,%20%E1%84%8E%E1%85%AE%E1%84%8E%E1%85%A5%E1%86%AB,%20%E1%84%8B%E1%85%B2%E1%84%89%E1%85%A1%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8C%E1%85%A6%E1%84%80%E1%85%A9%E1%86%BC%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%20%E1%84%80%E1%85%AE%E1%84%8E%E1%85%AE%E1%86%A8%202fbcf4f31dea42929748ab794be872aa/Untitled%2015.png)
    
    ![Untitled](%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8B%E1%85%AD%E1%84%8B%E1%85%A3%E1%86%A8,%20%E1%84%8E%E1%85%AE%E1%84%8E%E1%85%A5%E1%86%AB,%20%E1%84%8B%E1%85%B2%E1%84%89%E1%85%A1%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8C%E1%85%A6%E1%84%80%E1%85%A9%E1%86%BC%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%20%E1%84%80%E1%85%AE%E1%84%8E%E1%85%AE%E1%86%A8%202fbcf4f31dea42929748ab794be872aa/Untitled%2016.png)
    
    x이미지의 특징 추출하는 코드 
    
    ![Untitled](%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8B%E1%85%AD%E1%84%8B%E1%85%A3%E1%86%A8,%20%E1%84%8E%E1%85%AE%E1%84%8E%E1%85%A5%E1%86%AB,%20%E1%84%8B%E1%85%B2%E1%84%89%E1%85%A1%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8C%E1%85%A6%E1%84%80%E1%85%A9%E1%86%BC%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%20%E1%84%80%E1%85%AE%E1%84%8E%E1%85%AE%E1%86%A8%202fbcf4f31dea42929748ab794be872aa/Untitled%2017.png)
    
    위의 class를 통해 .npy 특징 파일을 미리 만들어 놓는 코드
    
4. 시스템 개요도
5. 플로우차트

## 대본 및 ppt

[https://www.miricanvas.com/v/12p50ie](https://www.miricanvas.com/v/12p50ie)

<제목페이지>
7조 발표 시작하겠습니다.<>

안녕하십니까 7조 발표를 맡은 최원석 입니다. 

시작하기에 앞서 여러분들 혹시 인터넷으로 물건은 많이 구매하시나요?
저는 주로 옷을 인터넷에서 구매하는 편이라 무신사, 인스타, 브랜드 사이트 등을 자주 이용합니다.

<>
이 프로젝트는 인터넷 쇼핑 중 불편한 경험을 바탕으로 시작되었습니다.

<>
제품을 살때 저희는 제품을 평가해서 삽니다.

간단하죠. 이 간단한 구조에서 저희가 어디에서 불편함을 느꼈는지 알려드리겠습니다.

<>
이곳은 제가 옷을 살때 자주 사용하는 사이트입니다. 

여기서 경험한 한가지의 경험을 토대로 설명을 드려보겠습니다. 

여러분들도 비슷한 경험이 있을 것입니다.
평소와 같이 저는 앵글런을 들어가서 옷을 구경하다가 마음에 드는 제품을 발견하고 구매를 진행했습니다.
설레는 마음으로 옷이 오기만을 기다리고 드디어 물건이 도착을 했는데 너무 큽니다…. 

색상도 원하던 느낌이 아니였고요. 

결국 반품을 해야했는데 여기서 무엇이 문제 였을까요?
바로 제가 평가를 잘 못한거죠…. 그러면 저는 어떻게 평가를 했어야 할까요??

<>
사이트에 들어가서 제품을 탐색하고, 

유사 제품 중에서 가성비가 좋은 것을 찾아보고, 

다른 제품들과 비교해보며 선택하고, 

선택한 제품의 사이즈를 정확히 측정하며,  

내 키 몸무게 팔 다리 허리사이즈 측정하고 유사한 체형을 가진 사람들과 어울리는지 확인하고, 

리뷰와 별점을 확인하며, 

거짓 리뷰를 구별하고, 

관련 제품에 대한 유튜브까지 검색하고 광고성인지 판단하고..

<>
저희는 어떤 제품을 살때 엄청나게 많은 정보를 하나하나 찾으러 여기 저기 돌아 다녀야합니다. 

물론 그 정보에 대한 신뢰도도 판단하고요. 저희는 여기서 문제점을 느꼈습니다.
왜 우리가 고생해서 찾아야할까요? 

Chat gpt가 시도 써주는 현대사회에서 이건 못해주나 이런 생각이 들었습니다. 

이것도 해줘. 그래서 full-review라는 사이트를 구상하게 되었습니다.
저희는 현재 신발을 기준으로 사이트를 구현하고 있으며 추후 여러가지의 종류로 사이트를 확장할 예정입니다.
저희는 이 사이트를 구현할때 총 4가지 단계를 생각했습니다. 

중요 4가지 단계 및 기능에 대해서 설명을 하고 플로우 차트와 시스템 개요도에 대해 설명을 하겠습니다.

total 요약 결과물:

 {'size_recommendations': '팀버랜드 6인치 부츠는 일반적인 신발 사이즈와 동일한 사이즈를 선택하는 것이 좋으며, 발볼이 넓은 분들은 반 사이즈 업하는 것을 추천합니다. 발이 작은 분들은 정사이즈를 고려해보세요. 개인의 발볼과 발등의 높이에 따라 사이즈를 조절할 수 있으므로, 착용하기 전에 직접 신어보고 편안한 사이즈를 선택하는 것이 좋습니다.', 'styling_suggestion': '팀버랜드 6인치는 다양한 스타일링에 활용할 수 있는 클래식하고 세련된 부츠이다. 청바지나 스키니진과의 조합으로는 캐주얼한 룩에 어울리며, 와이드한 바지와 매치하면 스트릿 스타일로 연출할 수 있다. 블랙 와이드 팬츠와 함께 하면 고급스러운 분위기가, 수에 팬츠와 함께 하면 자연스럽고 편안한 느낌을 줄 수 있다. 또한, 테일러드 슬랙스나 조거 팬츠와의 조합으로는 캐주얼한 비즈니스 스타일로도 연출할 수 있다.', 'unique_product_features': '팀버랜드 6인치 부츠는 완벽한 방수 기능과 내구성, 효율적인 보온성을 제공한다. 슬림한 실루엣과 스타일적인 매력도 특징이다. 편안한 착용감과 신축성도 견고한 환경에서도 유지된다. 스웨이드 소재로 제작되며, 생활방수 기능도 갖추고 있다. 디자인은 간결하고 무겁지 않은 특징을 가지고 있다.'}

<>—————————-—————————-—————————-—————————-
첫번째 크롤링 단계입니다.  

제품명, 카테고리, 주소재, 리뷰슈 이미지 url,리뷰 별점, 리뷰내용을 크롤링을 통해서 가져와 db에 저장합니다.

<>
두번째 요약 단계는 사용자가 입력한 제품에 대한 정보를 요약합니다. 

(유튜브만 요약 한 건 앞으로 나아갈 방안에서 말하기)
사용자가 제품을 입력하면 그 제품에 대한 유튜브 리뷰 영상을 요약 추출합니다. 

이때 사이즈 추천, 스타일링 제안, 제품 고유 특징, 제품 주요 키워드, 제품관련 설명을 추출합니다. 

요약 추출 방법은 youtube data api v3를 통해 입력제품 리뷰영상 id를 가져오고 youtube_transcript_api를 통해 영상에 대한 자막 데이터를 가져와 gpt api를 통해 3가지 지표에 대한 정보를 추출합니다. 

그리고 각 영상들의  공통 내용 취합해서 추출합니다.

다음은 팀버랜드 6인치 부츠라는 입력에 대한 추출 내용입니다.

(이 페이지에 코드들 그리고 요약 결과 사진으로 보여주기) 

현재 입력은 제품 이름으로만 입력을 받지만 추후 입력을 받을때 제품 사진으로도 입력을 받을 수 있게 구현 할 예정입니다. 결과를 잠시 확인해보겠습니다. 

<>
세번째는 추천도 계산입니다. Review-score(피피티 제목)
review-score 는여러가지 요소를 종합하여 측정합니다. 

감성 분석은 hugging face의 감성분석으로 파인튜닝된 모델 사용을 사용했습니다. 

이중 감성 분석은 리뷰의 긍 부정을 평가합니다. 

이 모델은 문장을 입력을 받아 다음처럼(사진 피피티에) 긍정인지 부정인지에 대한 확률을 보여줍니다. 

이러한 점수의 평균과 리뷰 개수 점수, 리뷰 평점 점수 이 세가지 점수에 가중치를 적용하여 종합 recommendation-score를 계산합니다. 

이는 이 제품을 추천해도 될지 평가하는 지표가 됩니다. 

추후에는 저희가 유저 피드백을 통해 가중치를 조절하고, 문장의 문자로만 긍 부정을 평가하는 것을 음성적인 지표도 확인하여 같은 단어내에서도 긍정과 부정을 평가할 수 있게, 그리고 좀 더 다양한 사이트에서 리뷰를 가져와 확실한 추천도를 계산할려고 합니다.

<>
네번째는 유사 제품 추천입니다.
제품에 대한 db에 저장된 이미지url을 가지고 VGG16모델을 이용해 제품에 대한 특징을 뽑습니다. 

db에 저장된 모든 신발을 이를 통해 특징들을 뽑고 그 값을 거리형태로 표현을 합니다. 

0~1값을 가지고 값이 적을수록 유사한 제품입니다.(코드) 이 이미지 유사도와  소재 유사도 그리고 카테고리 유사를 통합해 유사제품을 제공합니다. 

현재 소재 유사도/카테고리 유사도는 도메인 적 지식의 부족으로 단어적 유사도만 고려했으며 이를 극복해 좀더 완벽한 분류와 비슷한 소재와 카테고리의 관계에 대한 것을 수치화 할 예정입니다.

<>
위 단계는 다음과 같은 시스템 개요도와 프로우 차트를 가지고 구현됩니다.

플로우 차트는 앞서 설명드렸던 기능적이 내용이 들어가 있습니다. 

1단계 사용자가 제품명을 입력합니다.

2단계 입력된 제품명을 바탕으로 제품 기본 정보와 제품 영상 요약 데이터, 추천도를 보여줍니다. 기본 정보와 영상 요약 데이터를 추출하는 방식은 우측 플로우 차트와 같습니다.

크롤링을 통해 가져온 기본정보를 가져오고 youtube api 를 통해 비디오 제품에 관련된 영상 자막을 가져옵니다. 그리고 gpt api를 통해 3가지 지표로 압축해냅니다.

3단계 이미지, 소재, 카테고리를 입력제품과 유사한 상위 100제품을 추출합니다.

유사도 측정은 좌측 플로우차트와 같습니다. image_url을 바탕으로 미리 vgg16을 사용하여 제품 특징파일을 만들고 입력 제품의 특징파일과 비교하여 이미지적 유사도를 계산합니다. 나머지 소재, 카테고리적 유사도 또한 도메인 전문가와의 협업을 통해 만들어둔 벡터를 통해 코사인 유사도를 계산합니다. 그 후 각각의 설정된 가중치에 맞게 유사제품을 추출합니다.

그 뒤 100제품 중 추천도를 기준으로 30제품을 고른 후 유사제품으로서 전달됩니다.

4단계는 각 추천된 제품이 유용했는가를 기준으로 ㅇ가중치를 자동적으로 조절해 나갑니다.

시스템 개요도입니다. 
사용자의 입력은 검색창 입력을 통해 Nginx 웹 서버로 전달됩니다. 

Nginx는 정적 파일에 대한 요청을 바로 응답하거나, 동적 콘텐츠에 대한 요청을 Gunicorn으로 전달합니다. Gunicorn은 요청을 받으면 이를 Flask 웹 애플리케이션에 전달하며. 

Flask는 요청을 처리하기 위해 필요한 로직을 실행하고, YouTube Data API v3에서 동영상 관련 데이터를 가져온 후 앞서 설명했던 방식으로 gpt api를 통해 추천과 요약을 진행합니다. 

그리고 이에 관한 것들을 MySQL 데이터베이스에서 정보를 조회하거나 저장합니다.
처리가 완료된 후, Flask는 결과를 Gunicorn에게 반환하고, Gunicorn은 이를 다시 Nginx에게 전달하며 마지막으로, Nginx는 처리된 결과를 사용자에게 보내줍니다.
이 모든 시스템은 AWS Lightsail에서 호스팅되며, 안정적인 인터넷 연결과 리소스를 제공받아 운영됩니다.

<>
다음은 저희  출력 예시입니다. full-review는 메인 페이지에 원하는 상품을 검색하면 다음과 같은 출력을 제공합니다.
출력은 자세히 살펴보면 구성은 총 2가지로 나눌 수 있습니다.
정보페이지에서는 상품에 대한 객관적인 정보와 이를 이용한 사람들의 주간적인 정보가 요약되어 제공됩니다. 

이때 사이즈에/스타일링/상품 교유 특성에 대한 정보를 나눠서 보기 쉽게 제공합니다.

또한 사람들이 이 제품을 어떻게 평가했는 지 따라 추천도가 계산되어 제공됩니다.
 추천페이지에서는 검색한 상품과 유사한 상품을 추천도가 높은 순서로 제공을 합니다. 이때 디자인 유사도와 다른 지표들을 활용하여 제공을 합니다.
이를 통해 사용자는 내가 원하는 제품을 평가하기 위한 정보를 손쉽게 경험할 수 있게됩니다.

지금 보이는 화면은 팀버랜드 6인치 부츠에 대한 설명이며 사용자는 밑에 추천상품을 보다가 또 궁금한 상품이 있으면 이를 클릭해

<>

 다시 그 상품에 대한 정보와 이 상품과 비슷한 다른 추천 상품을 볼 수 있습니다. 스크롤을 하면 아래 27개의 제품이 더 있으며 제품 옆에는 추천도 지표가 있습니다.

<>
아직 부족한 부분이 있지만 충분히 해결 가능하며 이를 해결하면 맛있는 정보를 편하게 제공할 수 있을 거라고 확신합니다. 감사합니다.!

나이스~

ppt 적으로는 앞으로의 계획보다는 보완점.이라고 하는게 좋을듯함.

## 제품 시연용 자료

팀버랜드 6인치 프리미엄 부츠 10061

![Untitled](%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8B%E1%85%AD%E1%84%8B%E1%85%A3%E1%86%A8,%20%E1%84%8E%E1%85%AE%E1%84%8E%E1%85%A5%E1%86%AB,%20%E1%84%8B%E1%85%B2%E1%84%89%E1%85%A1%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8C%E1%85%A6%E1%84%80%E1%85%A9%E1%86%BC%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%20%E1%84%80%E1%85%AE%E1%84%8E%E1%85%AE%E1%86%A8%202fbcf4f31dea42929748ab794be872aa/Untitled%2018.png)

1. 제품1

[https://img.danawa.com/prod_img/500000/128/262/img/29262128_1.jpg?shrink=330:*&_v=20231024125715,4.5](https://img.danawa.com/prod_img/500000/128/262/img/29262128_1.jpg?shrink=330:*&_v=20231024125715,4.5)

![Untitled](%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8B%E1%85%AD%E1%84%8B%E1%85%A3%E1%86%A8,%20%E1%84%8E%E1%85%AE%E1%84%8E%E1%85%A5%E1%86%AB,%20%E1%84%8B%E1%85%B2%E1%84%89%E1%85%A1%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8C%E1%85%A6%E1%84%80%E1%85%A9%E1%86%BC%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%20%E1%84%80%E1%85%AE%E1%84%8E%E1%85%AE%E1%86%A8%202fbcf4f31dea42929748ab794be872aa/Untitled%2019.png)

제품명 : 팀버랜드 그린 스트라이드 Atwells Avenue 방수 처커 부츠 A5V1N

카테고리 : 부츠

주소재 : 천연가죽

1. 제품2

![Untitled](%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8B%E1%85%AD%E1%84%8B%E1%85%A3%E1%86%A8,%20%E1%84%8E%E1%85%AE%E1%84%8E%E1%85%A5%E1%86%AB,%20%E1%84%8B%E1%85%B2%E1%84%89%E1%85%A1%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8C%E1%85%A6%E1%84%80%E1%85%A9%E1%86%BC%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%20%E1%84%80%E1%85%AE%E1%84%8E%E1%85%AE%E1%86%A8%202fbcf4f31dea42929748ab794be872aa/Untitled%2020.png)

제품명 : CELINE 커트 레이스업 미드 부츠 - 누벅 카프스킨 & 시어링 라이트 탠/내추럴

카테고리 : 부츠

주소재 : 천연가죽

[https://www.celine.com/ko-kr/celine-커트-레이스업-미드-부츠---누벅-카프스킨-and-시어링-356774362C.18LN.39.html?gad_source=1&gclid=Cj0KCQiA4NWrBhD-ARIsAFCKwWv2fai8hgPcnlpYQNqkyRWooThEXVy8OXPEJxWArS7sz9EU83sifhsaAiHBEALw_wcB](https://www.celine.com/ko-kr/celine-%EC%BB%A4%ED%8A%B8-%EB%A0%88%EC%9D%B4%EC%8A%A4%EC%97%85-%EB%AF%B8%EB%93%9C-%EB%B6%80%EC%B8%A0---%EB%88%84%EB%B2%85-%EC%B9%B4%ED%94%84%EC%8A%A4%ED%82%A8-and-%EC%8B%9C%EC%96%B4%EB%A7%81-356774362C.18LN.39.html?gad_source=1&gclid=Cj0KCQiA4NWrBhD-ARIsAFCKwWv2fai8hgPcnlpYQNqkyRWooThEXVy8OXPEJxWArS7sz9EU83sifhsaAiHBEALw_wcB)

1. 제품 3

제품명 :****밀리터리 윌리 워커 (GK0GHU802CA)****

카테고리 : 부츠 

주소재 : 천연가죽

[https://abcmart.a-rt.com/product/new?prdtNo=7000013174&gad_source=1&BSCCN1=ABC&utm_campaign=shopping_pc&utm_medium=smartshopping&BSCPN=ABC&gclsrc=aw.ds&BSPRG=GRESP&utm_source=google&page=1](https://abcmart.a-rt.com/product/new?prdtNo=7000013174&gad_source=1&BSCCN1=ABC&utm_campaign=shopping_pc&utm_medium=smartshopping&BSCPN=ABC&gclsrc=aw.ds&BSPRG=GRESP&utm_source=google&page=1)

![Untitled](%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8B%E1%85%AD%E1%84%8B%E1%85%A3%E1%86%A8,%20%E1%84%8E%E1%85%AE%E1%84%8E%E1%85%A5%E1%86%AB,%20%E1%84%8B%E1%85%B2%E1%84%89%E1%85%A1%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8C%E1%85%A6%E1%84%80%E1%85%A9%E1%86%BC%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%20%E1%84%80%E1%85%AE%E1%84%8E%E1%85%AE%E1%86%A8%202fbcf4f31dea42929748ab794be872aa/Untitled%2021.png)

시연 제품 :

제품명:닥터마틴 워커 1460-BLACK

카테고리 : 부츠

소재 : 천연가죽

189000원

![Untitled](%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8B%E1%85%AD%E1%84%8B%E1%85%A3%E1%86%A8,%20%E1%84%8E%E1%85%AE%E1%84%8E%E1%85%A5%E1%86%AB,%20%E1%84%8B%E1%85%B2%E1%84%89%E1%85%A1%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8C%E1%85%A6%E1%84%80%E1%85%A9%E1%86%BC%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%20%E1%84%80%E1%85%AE%E1%84%8E%E1%85%AE%E1%86%A8%202fbcf4f31dea42929748ab794be872aa/Untitled%2022.png)

{'size_recommendations': '발볼이 눌리는 분들은 남성용 제품으로 나온 버전을 구매하시길 바랍니다. 그 편이 발볼이 넓은 편이라 추천됩니다. 발이 아플 수 있으니 반사이즈 업하는 것을 추천드립니다. 넉넉하게 신는 것을 추천합니다.',
'styling_suggestion': '닥터마틴 워커 1460-BLACK은 다양한 코디에 잘 어울리는 제품으로, 스키니 진이나 청바지와 함께 매치하거나 롱 원피스와도 잘 어울립니다 1461 스무스 모델은 아재 스타일이나 포스트맨 슈즈 스타일과 조합해 고급스러운 아재 스타일을 연출할 수 있고, 유니섹스 디자인이므로 남녀 모두에게 어울립니다 블랙 닥터마틴 워커 1460은 밀리터리 봄버 재킷과 청바지 혹은 블랙진과 함께 착용하는 것이 좋으며, 블랙 니트와 데님 팬츠, 체크 셔츠와 매칭하여 레트로하고 캐주얼한 스타일링도 가능합니다.',
'unique_product_features': '닥터마틴 워커 1460-BLACK은 블랙 컬러로 디자인되었으며, 유강한 힘이 있습니다 노란 스티치와 닥터마틴 상징인 마크가 특징이며, 발창은 스웨이드 소재로 되어 있습니다 마감처리가 깔끔하고 발볼이 넓어 편안한 착용감을 제공합니다 쿠션감이 좋고 내구성이 뛰어난 제품으로 21만원에 구매할 수 있습니다.'}

![Untitled](%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8B%E1%85%AD%E1%84%8B%E1%85%A3%E1%86%A8,%20%E1%84%8E%E1%85%AE%E1%84%8E%E1%85%A5%E1%86%AB,%20%E1%84%8B%E1%85%B2%E1%84%89%E1%85%A1%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8C%E1%85%A6%E1%84%80%E1%85%A9%E1%86%BC%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%20%E1%84%80%E1%85%AE%E1%84%8E%E1%85%AE%E1%86%A8%202fbcf4f31dea42929748ab794be872aa/Untitled%2023.png)

제품명 : Dr. Martens 레이스업 컴뱃 부츠

카테고리 : 부츠

주소재 : 천연가죽

198000원

![Untitled](%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8B%E1%85%AD%E1%84%8B%E1%85%A3%E1%86%A8,%20%E1%84%8E%E1%85%AE%E1%84%8E%E1%85%A5%E1%86%AB,%20%E1%84%8B%E1%85%B2%E1%84%89%E1%85%A1%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8C%E1%85%A6%E1%84%80%E1%85%A9%E1%86%BC%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%20%E1%84%80%E1%85%AE%E1%84%8E%E1%85%AE%E1%86%A8%202fbcf4f31dea42929748ab794be872aa/Untitled%2024.png)

제품명 : **닥터마틴 1460 W 유광 부츠 여성 워커 그레이**

주소재 : 천연가죽

카테고리 : 부츠

![Untitled](%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8B%E1%85%AD%E1%84%8B%E1%85%A3%E1%86%A8,%20%E1%84%8E%E1%85%AE%E1%84%8E%E1%85%A5%E1%86%AB,%20%E1%84%8B%E1%85%B2%E1%84%89%E1%85%A1%E1%84%8C%E1%85%A6%E1%84%91%E1%85%AE%E1%86%B7%20%E1%84%8C%E1%85%A6%E1%84%80%E1%85%A9%E1%86%BC%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%20%E1%84%80%E1%85%AE%E1%84%8E%E1%85%AE%E1%86%A8%202fbcf4f31dea42929748ab794be872aa/Untitled%2025.png)

제품명 : 망고 **레이스업 가죽 부츠**

카테고리 : 부츠

소재 : 소가죽

179000원
