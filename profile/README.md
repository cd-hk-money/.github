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

## 통신 개요도

![image](https://user-images.githubusercontent.com/68547545/175465406-22f034a7-96c7-4c36-b420-e3a56cb516b6.png)

```
1. 각 instance를 실행하여 Eureka Server에 등록
2. Client에서 API Gateway로 request
(3,4) API gateway에서 수신한 request를 어떤 instance에서 처리할 수 있을지  Service Discovery에서 찾음
5. API gateway가 client로부터 받은 request에 적합한 service instance에 request 전달
6. Service instance로부터 받은 response result 전달
```

## 시스템 구조

![image](https://user-images.githubusercontent.com/68547545/180674980-df11caa9-2c25-45ad-83c5-6fb1baf31fc1.png)


## API

![image](https://user-images.githubusercontent.com/68547545/175465976-b014a06b-6920-4697-a3bd-8f0b64fec9d4.png)
![image](https://user-images.githubusercontent.com/68547545/175465983-2e527eb3-9f8f-4fc3-9828-531829ac550f.png)
![image](https://user-images.githubusercontent.com/68547545/175465988-886be72c-82e3-420d-891d-cf12ec872619.png)


## 개발환경

<img src="https://img.shields.io/badge/vue.js-4FC08D?style=for-the-badge&logo=vue.js&logoColor=white"> <img src="https://img.shields.io/badge/springboot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white"> <img src="https://img.shields.io/badge/gradle-02303A?style=for-the-badge&logo=gradle&logoColor=white">

<img src="https://img.shields.io/badge/mysql-4479A1?style=for-the-badge&logo=mysql&logoColor=white"> <img src="https://img.shields.io/badge/mongoDB-47A248?style=for-the-badge&logo=MongoDB&logoColor=white"> 

<img src="https://img.shields.io/badge/java-007396?style=for-the-badge&logo=java&logoColor=white"> <img src="https://img.shields.io/badge/python-3776AB?style=for-the-badge&logo=python&logoColor=white"> <img src="https://img.shields.io/badge/javascript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black">


![image](https://user-images.githubusercontent.com/68547545/175466320-e5a4a34f-9cdd-4f35-a867-1a7c022e97fa.png)

