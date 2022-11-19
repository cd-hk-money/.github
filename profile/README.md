# 🔁 돈다

> 재무제표 기반 주식가격 평가 서비스 프로젝트 **'돈다'**

```
1. 돈다 단다. (동사) 저울로 무게를 헤아린다. “돈”은 아래아 발음.
2. 돈다. (형용사) 꿀이나 설탕의 맛과 같다.
3. 돈다. (동사) 물체가 일정한 축을 중심으로 원을 그리면서 움직이다.
4. 돈다. (동사) 기능이나 체제가 제대로 작용하다.
5. 돈(money) 다(all)
```

<br><br>

## 시스템 아키텍처 구성도

![image](https://user-images.githubusercontent.com/68547545/202846933-89b6feab-d269-4571-b6c7-06cf374575ea.png)

```

시스템은 크게 두 가지 서비스 모듈로 나눌 수 있습니다. 

1. **주식 데이터 모듈**(Python - FastAPI - RDBMS(MySQL)
2. **회원 모듈**(Java - Spring - In meory DB(Redis) - NoSQL DB(MongoDB))

문제 해결에 적합한 서비스 환경을 만들기 위해 모듈을 분리하였습니다.

주식 데이터 모듈의 경우 매일 업데이트되는 주식 가격 데이터와, 재무제표를 통한 2차 데이터 산출하기에 적합한 statistic 라이브러리(pandas, matplotlib 등)가 존재했고, 자동화에 용이한 python 환경으로 설계하였습니다.

회원 모듈은 회원 관리(회원 가입, 로그인/로그 아웃)와 관심 그룹, 관심종목 등록 기능과 같이 웹 클라이언트로부터 CRUD request를 받기에 적합한 Java-Spring 환경으로 설계하였습니다.

```

<br><br>

## 통신 개요도

![image](https://user-images.githubusercontent.com/68547545/180674980-df11caa9-2c25-45ad-83c5-6fb1baf31fc1.png)

```
1. 각 instance를 실행하여 Eureka Server에 등록
2. Client에서 API Gateway로 request
(3,4) API gateway에서 수신한 request를 어떤 instance에서 처리할 수 있을지  Service Discovery에서 찾음
5. API gateway가 client로부터 받은 request에 적합한 service instance에 request 전달
6. Service instance로부터 받은 response result 전달
```

## 입출력 개요도

![image](https://user-images.githubusercontent.com/68547545/180675860-69be1201-5172-4e8e-b9ac-aed3361a0714.png)


## 시스템 구조도

![image](https://user-images.githubusercontent.com/68547545/180675827-23b9a76f-7b91-4885-bdbc-c96dcf40249e.png)


## API

![image](https://user-images.githubusercontent.com/68547545/175465976-b014a06b-6920-4697-a3bd-8f0b64fec9d4.png)
![image](https://user-images.githubusercontent.com/68547545/175465983-2e527eb3-9f8f-4fc3-9828-531829ac550f.png)
![image](https://user-images.githubusercontent.com/68547545/175465988-886be72c-82e3-420d-891d-cf12ec872619.png)


## 개발환경

<img src="https://img.shields.io/badge/vue.js-4FC08D?style=for-the-badge&logo=vue.js&logoColor=white"> <img src="https://img.shields.io/badge/springboot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white"> <img src="https://img.shields.io/badge/gradle-02303A?style=for-the-badge&logo=gradle&logoColor=white">

<img src="https://img.shields.io/badge/mysql-4479A1?style=for-the-badge&logo=mysql&logoColor=white"> <img src="https://img.shields.io/badge/mongoDB-47A248?style=for-the-badge&logo=MongoDB&logoColor=white"> 

<img src="https://img.shields.io/badge/java-007396?style=for-the-badge&logo=java&logoColor=white"> <img src="https://img.shields.io/badge/python-3776AB?style=for-the-badge&logo=python&logoColor=white"> <img src="https://img.shields.io/badge/javascript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black">


![image](https://user-images.githubusercontent.com/68547545/175466320-e5a4a34f-9cdd-4f35-a867-1a7c022e97fa.png)

