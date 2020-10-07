# 📖 How Do Mo Do Project 

![version](https://img.shields.io/badge/version-0.0.1-orange?)![spring](https://img.shields.io/badge/spring-4.0.0-yellow?logo=spring)![spring-boot](https://img.shields.io/badge/springboot-4.0.0-yellow?logo=spring)[![mysql](https://jaywcjlove.github.io/sb/ico/mysql.svg)](http://www.mysql.com/)![aws-ec2](https://img.shields.io/badge/aws-ec2-blue)

### 🏠 [App Download Homepage](http://j3a305.p.ssafy.io:8080/home/index.html)

<hr>

### 📂 Contents

- [Project 소개](#-영화-관련-추천-서비스)
- [기술 스택](#-기술-스택)
- [사용 기술](#-사용-기술)
- [Git Flow](#-Git-Flow) 
- [역할분담](#-역할-분담)
- [Jira](#-jira)
- [화면 구성 Flow](#-화면-구성-Flow)

<hr>

### 🖥️ 영화 관련 추천 서비스

- 프로젝트 소개


<hr>

### 📃 기술 스택

이미지 첨부할 것

**BACKEND**

1. Programming Languages : [ Java 8 ] 
2. Frameworks : [ Spring ] 
   - Tool : [ Spring boot ]
3. SQL data storage : [ MySQL ]
5. Web Server : [ Nginx ]
6. Web application server : [ Apache Tomcat ]
7. Hosting : [ AWS ]

**FRONTEND**

1. Programming Languages : [ Kotlin ]
2. Framework Tool : [ Android Studio ]

**BigData/AI/Crawling**

1. Programming Languages : [ Python ]
2. Framework Tool : [ Django ] [ Spark ]
3. SQL data storage : [ MariaDB]
4. Hosting : [ AWS ]



<hr>

### 📃 사용 기술

#### [Backend]

> **Spring boot** : How Do Mo Do Project의 전반적인 기능 Rest Controller 구현
>
> **Swagger** : Swagger를 이용하여 RESTful API 문서 자동화
>
> **MySql** : 
>
> **AWS** : EC2 서비스를 이용하여 Ubuntu 서버를 구축(호스팅)
>
> **Nginx** : 웹서버를 구축



#### [Frontend]

> **MVVM**: MVVM (Model, View, View Model) 패턴을 활용하여 뷰 모델과 모델이 뷰로부터 독립적인 형태를 만들어서 UI로부터 				비즈니스 로직과 프레젠테이션 로직을 분리
>
> - 뷰는 **UI**와 **UI 로직**을 다룬다.
> - 뷰 모델은 **프레젠테이션 로직**과 뷰를 위한 **상태**를 다룬다.
> - 모델은 **비즈니스 로직**과 **데이터**를 다룬다.
>
> **Naver 검색 API**: 네이버 블로그 검색 결과를 출력해주는 REST API를 활용하여 영화에 대한 블로그 리뷰 View를 구성
>
> **Recycler View**: Recycler View를 활용하여 리스트화된 데이터를 효과적으로 보여줄 수 있도록 View를 구성
>
> - *Adapter* : 새로운 뷰의 추가를 위한 어뎁터
>   - 데이터를 가져와서 뷰에 적용
>   - Recycler View에게 View Holder를 전달
> - *View Holder* : 실제 아이템의 레퍼런스를 가지고 있고, 뷰에 새로운 데이터를 넣어 업데이트할 때 캐시로 사용  
>   - 'findviewbyid'를 Layout에 뷰가 추가될 때가 아닌 뷰가 생성될 때만 호출되게 최소화
> - *Layout Manager* : Recycler View에게 뷰를 어떻게 보여줄지 알려주는 역할
>   - 수직, 수평 , 그리드 등으로 보여주는거나 아이템을 추가 제거할때 애니메이션 효과 사용
>
> **Retrofit2**: API에 특화된 CRUD 방식의 웹 서버 연결을 편하게 구현할 수 있는 라이브러리를 활용하여 통신 작업을 진행
>
> **OkHttp**: HTTP & HTTP /2 통신 클라이언트 라이브러리를 활용하여 Request, Response 방식의 통신 활용
>
> **Glide**: 구글의 안드로이드 이미지 로딩 라이브러리인 Glide를 활용하여 Recycler View에 영화 포스터를 넣기 위해 사용
>
> **Koin AndroidX**: DI기술 사용을 위해 코틀린을 위한 DI 라이브러리 Koin AndroidX를 사용
>
> - **DI** (Dependency Injection): 의존성 주입 
>   - **구성요소간의 의존 관계가 소스코드 내부가 아닌 외부 설정 파일등을 통해 정의되게하는 디자인 패턴**
>     - EX) `카페에서 커피를 만드는데 커피 머신이 어떤 부품으로 구성되어있는지 바리스타는 알필요가 없다`
>     - 이렇게 분리시켜 놓으면 객체의 생성과 사용을 분리시킬 수 있고, 재사용이 유연해진다.
>   - `재사용성`을 높임
>   - `테스트`에 용이
>   - 코드를 `단순화`
>   - `종속된 코드`를 감축
>   - `결합도`를 낮추면서 `유연성`과 `확장성`이 향상
>
> **KAKAO Map**: 



#### [Big Data]

> **Pyspark**: pyspark 라이브러리를 활용하여 '19.09~'19.12 (4개월) 간의 카드사 데이터 분석
>
> - 데이터 전처리 및 SQLContext를 활용한 그룹핑 작업
>
> - persist()를 활용한 Action 결과 Dataframe 캐쉬 저장 (DISK AND CACHE)
>
> - 단계별 모듈화로 사전 분석을 통해 연산 과정을 단축시킴
>
> - 동일한 instance로 접근하여 생성한 cache값을 활용할 수 있도록 singleton pattern 적용
>
>   
>
> **Bertforsequenceclassification**:  Transformers의 pre-trained model 활용 (약 15만 개 리뷰 긍부정 데이터 학습)
>
> - 사전 학습은 Colab에서 진행
> - LSTM 대비 정확도 상승
> - Crawling을 활용하여 '네이버 영화' 페이지의 리뷰 두 페이지 분량 추출 및 평가 데이터 폼 구축
> - 현 개발환경에 GPU가 없어 상대적 속도 감소

<hr>

### 📃 Git Flow

- **MR / Pull Rule**

  - 스프린트 완료 후 일주일에 한번은 `develop`에 MR
  - `Front` / `Back` 에 각자 `Feature`를 MR,  `develop`  Pull 하여 최신화 

- **Commit Message Rule**

  `{상태} {기능} | {JIRA issue ID}`

  - ex)  `Feat Login Function | S03P11A305-1`
  - ex) `Update Movie Function Communication | S03P11A305-2` 
  

  `[마무리] | {날짜 }| {JIRA issue ID}`

  - ex) `[마무리] | 2020.07.21 | S03P11A305-1`
  

  `[MR] | '{소스브랜치}' into '{타겟브랜치}'`

-  **진행상황** 
>  - Todo
>  - In Progress
>  - Done

- **Git Branch 전략**

  - Master

    - Develop

      - Front

        - Front_doc
        - Front_epic Name
- Back
      
  - Back_doc
        - Back_epic Name
      - bigdata_recommand
      - pn_score_analysis
      
    - release
    
      

### 📃 역할 분담

- PM

  🕵‍♂ **이선수**

- Frontend

  👱 **김찬영** 👨 김대용 👦 김형택

  ```markdown
  # [Role]
  ## [김 찬 영]
  
  ## [김 대 용]  
  
  ## [김 형 택]
  ### 1. Main Page
  	- 1) Recycler View를 통한 실시간 상영 영화 정보 구성
      	- 실시간 상영 영화 API 활용
      	- 예매하기 버튼을 클릭하여 해당 영화에 대한 긍정/부정 분석 결과를 Dialog로 출력
      		- BigData 분석 결과를 통한 긍정/ 부정 점수를 통신하고 결과값을 받아와 Dialog에 적용
      	- 영화관 선택 화면으로 연결
      - 2) Recycler View를 통한 영화 블로그 리뷰 정보 구성
      	- Spinner를 통해 영화를 선택
      	- 선택된 영화를 네이버 블로그 검색 API 활용
      	- Web View Activity를 활용하여 해당 블로그로 연결
  ### 2. Login Page
  	- 1) Login Activity, View Model, layout을 통해 view를 구성
  	- 2) Backend 파트와 로그인 관련 통신
  ### 3. MyPage
  	- 1) 회원정보 수정 Activity, View Model, layout을 통해 view를 구성
  	- 2) 회원 탈퇴 Activity, View Model, layout을 통해 view를 구성
  	- 3) Backend 파트와 회원정보 수정, 탈퇴 기능 통신
  ### 4. Dialog Activity
  	- 1) 회원 탈퇴 및 영화 리뷰 긍정/부정 분석 정보 Dialog Activity를 구현
  	- 2) 사용자에게 효과적으로 보여질 수 있도록 layout을 구현
  ### 5. Splash Page
  	- 1) App 처음 실행 화면 Splash Activity, layout을 통해 view를 구성
  ```

  

- Backend

  👨 **권오정** 👩 전수현

- Big Data

  👨 **이선수**

  ```markdown
  # [Role]
  ## [이선수]
  ### 1. bigdata analysis of activitiy 
  	- 1) spark 세션 생성 및 분석 데이터 로드
  	- 2) 시구군 기준 그룹핑 dataframe 생성
  	- 3) param에 따른 dataframe 분석
  	- 4) 결과값 response (json)
  	- 5) Django RESTful api 활용 (GET)
  	- 6) python 모듈화 및 singleton pattern 적용 (여러 세션의 접근에 동일한 사전분석 데이터를 		활용하기 위해)
  ### 2. positive/negative score analysis
  	- 1) Bertforsequenceclassification 15만개 긍부정 리뷰 사전 학습 및, 학습 모델 추출			(Colab 환경에서 학습 후 추출) 
  	- 2) Crawling을 통해 '네이버 영화' 홈페이지의 리뷰 2페이지 분량 추출
  	- 3) 평가 데이터 토큰화 및 어텐션 마스킹, 파이토치의 텐서형으로 변환
  	- 4) Django RESTful api 활용 (GET)
  	- 5) python 모듈화 및 singleton pattern 적용 (여러 세션의 접근에 동일한 사전분석 데이터를 		활용하기 위해)
  	- 6) AWS 환경설정 및 배포 관리
  ```
  
  

### 📃 Jira

##### 프로젝트 관리 도구로 Jira를 사용, Issue를 등록하여 프로젝트를 진행

- Epic : 전체적인 큰 기능들을 Epic으로 구성
  - Ex) Front | User Function (회원 관리) , Back | Theater Function (상영관)

- Story : Epic과 연결하고 Epic에 관련된 기능 구현을 위주로 구성
  - Ex) Front | Main Page , Back | Movie CRUD, BigData | 긍부정 분석 
- Bug : 테스트 과정에서 발견된 bug를 등록
  - Ex) Front | Kakao Map



### 📃 화면 구성 Flow

#### 홈 화면

![image](https://user-images.githubusercontent.com/45157374/95287243-593ea780-08a0-11eb-9b9c-9311a42c1313.png)



- 현재 상영중인 영화리스트를 상단에 가로 형태로 보여줍니다. (네이버 영화 크롤링)

- 하단에 영화 제목으로 네이버 블로그 검색결과를 보여줍니다. -> 영화의 후기를 참조 할 수 있습니다.

- 예매하러가기 클릭 시 예매 플로우로 들어가게 됩니다.

