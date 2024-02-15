## 📚 Table of Contents

- [DEPLOY URL](#deploy-url)
- [SPECIFICATION](#specification)
- [INTRODUCTION](#introduction)
- [SERVICE LAYOUT](#service-layout)
- [SKILLS](#skills)
- [SYSTEM ARCHITECTURE](#system-architecture)
- [ERD](#erd)
- [FEATURES](#features)
- [DEVELOPERS](#developers)

<br>

---

## Deploy URL

- ✅ front-server : https://i10a608.p.ssafy.io
- ✅ back-server : https://i10a608.p.ssafy.io/api

<br>

## Specification
- notion: https://aquamarine-casquette-a56.notion.site/Dashboard-70656f0c8c97466b8b282bec9b190947?pvs=4
---

## Introduction

### main-service

- 우리 아이를 위한 플래너부터 기록까지 한 번에 해결!
- 금쪽 플래너를 통해 아이와의 활동을 체계적으로 계획하고 관리할 수 있다.
- 아이와 함께 할 일 추천부터 함께 할 시간을 설정하고 내가 만들었던 계획을 단위별로 확인 가능하다.

- 금쪽 일기를 통해 아이와 함께한 특별한 순간, 발달상의 진전 등을 기록할 수 있다.
- 일기는 캘린더를 통해 날짜별로 확인할 수 있고 모음으로 한 눈에 확인할 수도 있다. 
- 작성을 하던 중 일이 생긴다면 임시저장 기능을 활용해 다음에 이어 쓸 수 있다. 

### sub-service

- 마이페이지를 이용한 내 아이 관리와 회원 관리

- 내가 육아 스트레스로 인해 힘들지는 않은지 아이가 발달장애가 의심되지 않는지 확인하는 자가진단 기능
- 나와 다른 부모들이 아이를 잘 키울 수 있도록 꿀팁을 서로 공유하는 꿀팁 게시판 

<br>

---

## Service Layout

### 메인
<img src="https://private-user-images.githubusercontent.com/79824230/305008696-61bea434-8e3d-4e41-bb49-18d61afebcab.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MDc5ODc0MTYsIm5iZiI6MTcwNzk4NzExNiwicGF0aCI6Ii83OTgyNDIzMC8zMDUwMDg2OTYtNjFiZWE0MzQtOGUzZC00ZTQxLWJiNDktMThkNjFhZmViY2FiLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDAyMTUlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQwMjE1VDA4NTE1NlomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTI4OWQ1YmQyNmJmYzQ5ZDVhM2E5MjYxYWQ3NzhjYTk0OWI0NzJkM2VhZmE4YzAyMzg3ODE0OTlmZGQwYzliMDYmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.vcmnS0TbDFWsSsJf0mnwwKXtkBpN0jKs8fVUYF1hLxg" width="800" alt="main">

### 금쪽 플래너
<img src="https://private-user-images.githubusercontent.com/79824230/305009644-99773b1e-076e-4ce4-aac9-12426db459e1.gif?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MDc5ODc3NjgsIm5iZiI6MTcwNzk4NzQ2OCwicGF0aCI6Ii83OTgyNDIzMC8zMDUwMDk2NDQtOTk3NzNiMWUtMDc2ZS00Y2U0LWFhYzktMTI0MjZkYjQ1OWUxLmdpZj9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDAyMTUlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQwMjE1VDA4NTc0OFomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWQ5NjI2NWM0OWI2Nzg5YmRhYTVlY2FjZTNjM2JlZmFjZTA4ZTljZWYzYThkMjJlMTJiMWJiZDE4ZjliMjZjZWYmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.J6YZYld1vvRrIVbr85yxdTUGfRc145auBvA0C9A_mv0" width="800" alt="plan">

### 금쪽 다이어리
<img src="https://private-user-images.githubusercontent.com/79824230/305009513-a4c77512-f883-429b-aeb8-3a8b64e4c581.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MDc5ODc2NDEsIm5iZiI6MTcwNzk4NzM0MSwicGF0aCI6Ii83OTgyNDIzMC8zMDUwMDk1MTMtYTRjNzc1MTItZjg4My00MjliLWFlYjgtM2E4YjY0ZTRjNTgxLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDAyMTUlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQwMjE1VDA4NTU0MVomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTY1ODcyZmVlMGIyYTM1YWQxNzg5OTY3NWUzNDFhN2FhNTFmODczNDU3YzVkZTNiY2NiYjRmY2MyY2I4NzRiNTMmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.xj4unIpwnPmS1IAW1hA4c1YqJSLDg_QdxSHYiZlk9p8" width="800" alt="diary">


### 자가진단
<img src="https://private-user-images.githubusercontent.com/79824230/305009086-c087b6c4-bad5-47dd-a132-e1ce2ed7bb25.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MDc5ODc2NjgsIm5iZiI6MTcwNzk4NzM2OCwicGF0aCI6Ii83OTgyNDIzMC8zMDUwMDkwODYtYzA4N2I2YzQtYmFkNS00N2RkLWExMzItZTFjZTJlZDdiYjI1LnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDAyMTUlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQwMjE1VDA4NTYwOFomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWFmZTRjMTVjMmEzYTY2YWU1NzVhM2MzNTQzNDM2Njk1ODk3NTBiZDYyNDVmZTVjNTBiZGZhMzMzZDU1YjdmZGUmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.YDIYsPF_PL20P5cmYSpEph6yjXir52h2Ta8nwEC1vPw" width="800" alt="survey">

### 꿀팁 게시판
<img src="https://private-user-images.githubusercontent.com/79824230/305008932-dd9de101-3d6d-4ebd-b220-c7d11adec055.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MDc5ODc3MjEsIm5iZiI6MTcwNzk4NzQyMSwicGF0aCI6Ii83OTgyNDIzMC8zMDUwMDg5MzItZGQ5ZGUxMDEtM2Q2ZC00ZWJkLWIyMjAtYzdkMTFhZGVjMDU1LnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDAyMTUlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQwMjE1VDA4NTcwMVomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTk2YTY4MDM5ZWU1NGQ0NTM2ZjFjNGY0ZGJmMmU1YTkxMmMxYTJlNTc4NzRiNmE4ODk3OTIxOGI2YmFiM2FkYzImWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.grbf7yggAEKdBWuv0NXtkxJcPfZn1dyNqdmYM47UqYA" width="800" alt="article">

<br>

---

## Skills

### language

    - back: Java 17
    - front: JavaScript, Vanilla CSS

### framework

    - back: SpringBoot 3.2.1, MyBatis 3.0.3
    - front: Vue3

### skills

    - back: Spring Security 6.2.1, JWT
    - front: Pinia, Vue Router

### database

    - MySQL 8.0.36

### server

    - AWS EC2
    - Docker
    - Nginx
    - Jenkins

--- 

## System Architecture
<img src="https://private-user-images.githubusercontent.com/79824230/305009286-994936f1-1ffb-4600-80e1-38f1085923ce.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MDc5ODc4MTgsIm5iZiI6MTcwNzk4NzUxOCwicGF0aCI6Ii83OTgyNDIzMC8zMDUwMDkyODYtOTk0OTM2ZjEtMWZmYi00NjAwLTgwZTEtMzhmMTA4NTkyM2NlLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDAyMTUlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQwMjE1VDA4NTgzOFomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTdjMzk3Mjg2NDkyOTllN2RhYTg3ODNjMDgzOTRjZTM3OTYzMzIzMGUzNjEyYmYxNzNmMjJjODEzMTY3ZGVmMDgmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.xtkfp99F9bH-reTrAr2bg7EQy4wP2jCFLTcqaO_lBS8" width="800" alt="architecture">

---

## ERD
<img src="https://private-user-images.githubusercontent.com/79824230/305012068-c6c35453-4b88-4fdf-a867-3af4c5f44a59.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MDc5ODc4NjQsIm5iZiI6MTcwNzk4NzU2NCwicGF0aCI6Ii83OTgyNDIzMC8zMDUwMTIwNjgtYzZjMzU0NTMtNGI4OC00ZmRmLWE4NjctM2FmNGM1ZjQ0YTU5LnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDAyMTUlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQwMjE1VDA4NTkyNFomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTQzNGRkYTA3YTFmY2YwNzU3OTc2Y2UxYTFlZGVkZDVhNDQyYmRkYzFjMGUwYzhkNTU1NzAzMzAwZTdlOTQwMGImWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.HhCaNNrezplnf41GdnqCxjW0UpIOImvLeHtSto9y2gE" width="800" alt="ERD">


---

## Features

### 🎯 금쪽 플래너 
- [x] 내가 설정한 기간 단위의 플래너
- [x] 모든 계획에 시간을 설정해 아이와 함께 하는 시간 추적
- [x] 계획 추천 기능으로 클릭만으로 간단한 플래너 구성
- [x] 완성된 플래너를 조회하고 끝난 행동은 삭제

### 🎯 다이어리
- [x] 다이어리 작성 (작성 중 임시 저장 가능)
- [x] 캘린더뷰를 이용한 날짜별 일기 미리보기 기능
- [x] 일기모음을 이용한 모든 일기 보기와 일기 내용 보기
- [x] 파일 업로드 기능을 활용한 다이어리 내 이미지 추가 기능

### 🎯 자가진단
- [x] 육아 스트레스로 인한 부모의 우울증 진단
- [x] 간단 설문을 통한 ADHD 의심 증상 진단 

### 🎯 꿀팁 게시판
- [x] 게시판 기본 기능 (글 전체 보기, 글 상세 보기, 작성, 수정, 삭제)
- [x] 필요한 파일 공유를 위한 파일 업로드 & 다운로드 
- [x] 글 제목, 내용, 유저 닉네임 검색 기능
- [x] 댓글 기능 (조회, 작성, 수정, 삭제) 
- [x] 게시글 추천 기능
---

## Developers

|||||||
|:-:|:-:|:-:|:-:|:-:|:-:|
|<img src="https://github.com/kjy0349.png" width="190">|<img src="https://github.com/kimgiraffe.png" width="190">|<img src="https://github.com/dkdo1406.png" width="190">|<img src="https://github.com/Hunnibs.png" width="190">|<img src="https://github.com/so2043.png" width="190">|<img src="https://github.com/d2doo.png" width="190">|
|[김제영](https://github.com/kjy0349)|[김세민](https://github.com/kimgiraffe)|[김형중](https://github.com/dkdo1406)|[이병헌](https://github.com/Hunnibs)|[정소영](https://github.com/so2043)|[정지수](https://github.com/d2doo)|
|INFRA||||DESIGN|DESIGN| 
|BE & FE|FE|BE & FE|BE & FE|FE|FE|
