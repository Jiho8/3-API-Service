
<!-- ![2ndProjectMockup](https://github.com/user-attachments/assets/de838a7c-acea-45ba-abd3-17ec3a848838) -->
<!-- ![2ndProjectMockup_2](https://github.com/user-attachments/assets/146c115c-d1fb-45ef-a5c0-fa77351f8786) -->
![mockup_ttunabobseo](https://github.com/user-attachments/assets/4371d04e-e9ce-4651-a8b5-a2027865b680)

# <p><img src="https://github.com/user-attachments/assets/62fac1aa-5182-40b6-9ca3-6505f3f24fa7" alt="Image" style="vertical-align: middle;" /> 떠나봅서</p> 
'떠나봅서'는 제주 여행에 특화된 정보 탐색 및 사용자 간 소통을 위한 웹 플랫폼입니다. React.js 기반의 SPA로 개발되어 페이지 이동 없이 빠르고 매끄러운 사용자 경험을 제공합니다.

비짓제주와 기상청 오픈 API를 활용해 실시간 관광지, 맛집, 행사 정보를 제공하며, 개인화된 여행 준비를 돕기 위해 일정 및 준비물 관리 기능을 통합했습니다. <br>
사용자는 커뮤니티를 통해 정보를 공유하고 소통할 수 있으며, SNS 로그인으로 편리하게 이용 가능합니다.

이 프로젝트를 진행하며 백엔드(Node.js, Express)와의 연동 경험과 MongoDB 활용 능력을 쌓았습니다. <br>
또한, useState, useEffect 등 React 훅에 대한 이해도를 향상시키고, 효율적인 서버 통신 및 로컬/세션 스토리지 활용을 통해 실질적인 프론트엔드 개발 역량을 강화했습니다.

## 🔗 배포 URL
* 프론트: https://jeju-trip-eosin.vercel.app
* 서버: https://jeju-server.vercel.app
* 서버 Github: https://github.com/Jiho8/Jeju-server

## 📑 프로젝트 요약

### 1. 주제
제주 여행에 특화된 정보 탐색 및 사용자 간 소통 플랫폼

* 여행 준비를 위한 정보 제공
* 일정 및 준비물 관리 기능
* 여행자 커뮤니티 기능

### 2. 목표

* 비짓제주, 기상청 오픈 API를 활용해 실시간 정보 제공 및 개인화된 여행 서비스 제공
* 다양한 정보 및 관리 기능을 통해 여행자들의 편의성 향상

### 3. 주요 기능

* SPA (Single Page Application) 기반으로 페이지 이동 없이 빠른 이용 경험 제공
* 관광지, 맛집, 행사 등 다양한 장소 정보 제공
* 커뮤니티를 통한 소통 및 정보 공유
* 일정 작성/관리 및 여행 기간별 추천 일정
* 여행 준비물 체크리스트
* 소셜 로그인 (카카오·구글·네이버)
* 마이페이지 제공
* 반응형 UI (모바일 480px, 태블릿 768px)

### 4. 주요 기술 스택

* Front-End : React, Zustand, React Router
* Back-End : Node.js, Express, MongoDB
* API 활용 : 비짓제주 Open API, 기상청 Open API

## 📆 기간 및 인원

  * 총 작업 기간 : 15일
    * 기초 데이터 수집 및 화면 설계 기간 : 2일
    * 개발 및 테스트 기간 : 13일
   
  * 팀원 : 5명

## 👩🏻‍🤝‍🧑🏻 팀원 소개

| 이름 | 담당 | 주요 페이지 컴포넌트 | 해당 |
| :---:| :---: | :---: | :---: |
| 소연희 | 팀장/디자인 | Home.jsx, 장소 정보 (trip 폴더) | |
| 안지현 | 기획/개발 | 내 여행 일정 (planner 폴더) | |
| 천지호 | 개발/배포 | 마이페이지 (mypage 폴더), 로그인 (sns) | ✔ |
| 황수빈 | 기획 | 커뮤니티 (community 폴더) | |
| 이용욱 | 리소스 수집 | mypage 폴더 내 Like.jsx, QnA.jsx | |

## 💡 기능 구현 상세

### 1. 제주비짓 API 활용
* 비짓제주 오픈 API를 활용하여 메인 콘텐츠, 검색 기능, 방문자 통계 등 제주 지역의 다양한 장소 및 행사 정보를 동적으로 제공.
* **Axios**를 이용한 비동기 데이터 요청 및 응답 처리를 구현하고, **Zustand**를 통해 전역적으로 상태를 효율적으로 관리.
* trip 페이지 컴포넌트 내 맛집, 관광지, 포토스팟, 소품샵 등 제주 장소 정보를 카테고리별로 분류하고 렌더링.
* 홈의 메인 슬라이드는 데이터를 랜덤으로 가져와 **로컬 스토리지에 24시간 동안 저장**하여 불필요한 API 호출을 줄이고, 이후 새로운 데이터를 가져와 표시하여 성능 최적화

### 2. 기상청 API 활용
* **기상청 API**와 연동하여 현재 위치 기반 또는 제주도 전체의 실시간 날씨 정보(Home.jsx) 제공.
* `PlannerDetail.jsx`에서 오늘부터 최대 10일까지의 상세 주간 날씨 예보를 파싱하여 사용자에게 여행 계획에 필요한 정보 제공.
* API 응답 데이터를 가공하여 사용자 친화적인 날씨 아이콘 및 정보로 변환하여 표시.
* **Express**를 활용한 자체 API 서버를 통해 기상청 API와 안전하게 통신하여 클라이언트의 직접적인 API 키 노출을 방지하고 요청을 관리.

### 3. 트립
* 각 카테고리당 **랜덤으로 5개의 데이터를 가져와 화면에 표시**하고, **로컬 스토리지에 24시간 동안 저장**하여 재방문 시 빠른 로딩 지원. 
* 각 장소에 대한 **'좋아요' 기능**을 구현하여 사용자 관심사를 반영하며, **사용자 ID를 기반으로 MongoDB 데이터베이스에 해당 정보 저장 및 관리**.
* 클릭한 장소의 데이터를 기반으로 **주변 관광지를 추천하는 로직** (예: 장르, 태그, 위치 데이터 활용 등)을 구현하여 사용자 탐색 경험 확장.

### 4. 떠나톡 (커뮤니티)
* **Node.js, Express**를 활용한 백엔드 서버를 구축하여 게시글 및 댓글 데이터의 **CRUD(생성, 읽기, 업데이트, 삭제)** 로직 처리.
* **MongoDB**를 데이터베이스로 사용하여 유연한 스키마 설계 및 데이터 저장/관리를 담당. 
* 여행자들이 서로 정보를 공유하고 소통할 수 있는 게시글 작성/조회, 댓글, 좋아요 기능 구현.
* '떠나팁' 섹션을 통해 관리자들의 제주 여행 관련 유용한 정보를 체계적으로 제공.

### 5. 내 여행 플래너 기능
* **MongoDB와 Express**를 백엔드로 활용하여 사용자의 여행 일정을 생성, 수정, 삭제(CRUD) 및 조회하는 기능 구현.
* **Zustand**를 이용하여 여행 일정 관련 전역 상태를 효율적으로 관리하여 컴포넌트 간 props 전달을 최소화하고 일관된 데이터 흐름을 유지.
* 사용자가 직접 쉽고 편리하게 여행 계획을 세울 수 있도록 직관적인 UI/UX를 제공하며, 일정별 장소 추가 및 관리가 가능.
* 1박 2일, 2박 3일 등 여행 기간에 맞춘 추천 일정을 제공하여 사용자의 계획 수립을 돕는 보조 기능을 제공.

### 6. 마이페이지
* **카카오, 구글, 네이버 SNS 로그인**을 통해 사용자 인증 및 개인화된 서비스 제공.
* 로그인한 사용자 정보는 **MongoDB에 저장 및 관리**되어, 각 사용자에게 맞춤형 서비스(게시글, 댓글, 좋아요 목록 등)를 제공하는 기반이 됨.
* **Express 서버와 MongoDB**를 연동하여 체크리스트 확인 및 관리. 사용자가 필요한 물품을 추가/수정/삭제하며 체계적으로 관리할 수 있도록 지원하며, 이 데이터는 **사용자 ID를 기반으로 MongoDB에 저장 및 관리**.
* 내가 작성한 게시글, 댓글 목록 조회 기능 및 좋아요한 게시글, 장소 목록 조회 기능을 구현하여 사용자 활동 내역을 한눈에 확인 가능.

## 🗂️ 폴더 구조

```
📂Jeju
┣ 📂Jeju-trip                 # 떠나봅서 ( Front-End 프로젝트 )
┃ ┣ 📂public
┃ ┃ ┣ 📂imgs                  # 로고 등 정적 이미지 폴더
┃ ┃ ┃ ┗ 📂_icons
┃ ┣ 📂src
┃ ┃ ┣ 📂component             # 컴포넌트 폴더
┃ ┃ ┃ ┣ 📂_common             # 공통 컴포넌트 폴더
┃ ┃ ┃ ┣ 📂00-login            # 로그인 컴포넌트 폴더
┃ ┃ ┃ ┣ 📂00-search           # 검색 컴포넌트 폴더
┃ ┃ ┃ ┣ 📂01-home             # 홈 컴포넌트 폴더
┃ ┃ ┃ ┣ 📂02-trip                 
┃ ┃ ┃ ┃ ┣ 📂tripDetail        # 장소 상세 페이지 컴포넌트 폴더
┃ ┃ ┃ ┃ ┗ 📂tripList          # 장소 리스트 페이지 컴포넌트 폴더
┃ ┃ ┃ ┣ 📂03-community
┃ ┃ ┃ ┃ ┣ 📂comment           # 댓글 컴포넌트 폴더
┃ ┃ ┃ ┃ ┣ 📂img               # 갤러리 컴포넌트 폴더
┃ ┃ ┃ ┃ ┗ 📂post              # 게시물 컴포넌트 폴더
┃ ┃ ┃ ┣ 📂04-planner
┃ ┃ ┃ ┃ ┣ 📂calendar          # 달력 컴포넌트 폴더
┃ ┃ ┃ ┃ ┣ 📂plannerDateil     # 내 일정 상세 페이지 컴포넌트 폴더
┃ ┃ ┃ ┃ ┣ 📂search            # 장소추가 컴포넌트 폴더
┃ ┃ ┃ ┃ ┣ 📂ticket            # 내 여행 일정의 하루 단위 티켓 컴포넌트 폴더
┃ ┃ ┃ ┃ ┗ 📂weather           # 내 여행 내 오늘 ~ 10일까지 날씨 컴포넌트 폴더
┃ ┃ ┃ ┣ 📂05-mypage
┃ ┃ ┃ ┣ 📂icons               # 아이콘 컴포넌트 폴더
┃ ┃ ┃ ┗ 📂popups              # 팝업 컴포넌트 폴더
┃ ┃ ┣ 📂pages                 # 각 페이지 컴포넌트 폴더
┃ ┃ ┃ ┣ 📂00-search
┃ ┃ ┃ ┣ 📂01-home
┃ ┃ ┃ ┣ 📂02-trip
┃ ┃ ┃ ┣ 📂03-community 
┃ ┃ ┃ ┣ 📂04-planner
┃ ┃ ┃ ┣ 📂05-mypage
┃ ┃ ┃ ┃ ┗ 📂check             # 체크리스트 페이지
┃ ┃ ┃ ┗ 📜Splash.jsx          # 인트로 페이지
┃ ┃ ┣ 📂styles                # scss
┃ ┃ ┣ 📂utils                 # 로그아웃.js
┃ ┣ 📜api.js                  # zustand 전역 상태 관리
┃ ┗ 📜App.js                  # 프로젝트의 전체 라우팅 및 최상위 컴포넌트
┣ ⚙️.env
┗ README.md
┣ 📂Jeju-server               # 떠나봅서 ( Back-End 프로젝트 )
┃ ┣ 📂api                     # API 호출 및 가공하는 라우터 폴더
┃ ┣ 📜index.js                # 서버의 메인 파일, 라우터를 연결하고 서버를 실행
┗ ┗ ⚙️.env
```

## 💻 개발 환경

### 1. Frond-End

| 사용기술 | 설명 |Badge |
| :---:| :---: | :---: |
| **React** | **프론트엔드 프레임워크 (SPA 구축)** |![react](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=white)|
| **React Router Dom** | **페이지 라우팅 관리** |![reactrouter](https://img.shields.io/badge/ReactRouter-CA4245?style=flat-square&logo=reactrouter&logoColor=white)|
| **React Hook Form** | **폼 데이터 관리** |![reacthookform](https://img.shields.io/badge/ReactHookForm-F24E1E?style=flat-square&logo=reacthookform&logoColor=white)|
| **Axios** | **HTTP 클라이언트 라이브러리** |![axios](https://img.shields.io/badge/Axios-5A29E4?style=flat-square&logo=axios&logoColor=white)|
| **Zustand** | **상태 관리** |![Zustand](https://img.shields.io/badge/Zustand-181717?style=flat-square&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABQAAAAUCAYAAACNiR0NAAAACXBIWXMAAA7EAAAOxAGVKw4bAAAAv0lEQVQ4jeVUMQ7DIAx0KmZGlJGJB+RBjLyC1/ADVr7AC8gzCBJs7lCpUhqw0qpDqp7kxSefDWd5QkQYwVqLQogh/4oYIwAiDiOlhO/AOYe30+1P4g8FGUUqpSaC7q4Hs9ai1rorFkJAKeUuX0qBZVmGjZgQApRSXVJKeeByzsTQv2DK911urXX/hXMOpZQDt20bcM67NbVWmKjj8AnIJ6/rivDYt2fknMkJrm/K9QXJ4+C9h3med7laKxhjhjV3vjqJYwKihcAAAAAASUVORK5CYII=&logoColor=white)|
| **Node.js** | **JavaScript 런타임 환경 (프론트엔드 개발 및 빌드 도구 실행용)** |![nodedotjs](https://img.shields.io/badge/Node.js-5FA04E?style=flat-square&logo=nodedotjs&logoColor=white)|

### 2. UI/UX & 날짜/시간 라이브러리

| 사용기술 | 설명 | Badge |
| :---:| :---: | :---: |
| **MUI** | **UI 프레임워크** |![mui](https://img.shields.io/badge/MUI-007FFF?style=flat-square&logo=mui&logoColor=white) |
| **Swiper** | **슬라이더** |![Swiper](https://img.shields.io/badge/Swiper-6332F6?style=flat-square&logo=axios&logoColor=white)|
| **react-swipeable** | **스와이프 제스처** |![npm](https://img.shields.io/badge/react--swipeable-00e6a4?style=flat-square&logo=npm&logoColor=white)|
| **motion** | **애니메이션** |![motion](https://img.shields.io/badge/motion-fff312?style=flat-square&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHhtbG5zOnhsaW5rPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hsaW5rIiB2aWV3Qm94PSIwIDAgMjQgOSI+CiAgPHBhdGggZD0iTSA5LjA2MiAwIEwgNC4zMiA4Ljk5MiBMIDAgOC45OTIgTCAzLjcwMyAxLjk3MSBDIDQuMjc3IDAuODgyIDUuNzA5IDAgNi45MDIgMCBaIE0gMTkuNjU2IDIuMjQ4IEMgMTkuNjU2IDEuMDA2IDIwLjYyMyAwIDIxLjgxNiAwIEMgMjMuMDA5IDAgMjMuOTc2IDEuMDA2IDIzLjk3NiAyLjI0OCBDIDIzLjk3NiAzLjQ5IDIzLjAwOSA0LjQ5NiAyMS44MTYgNC40OTYgQyAyMC42MjMgNC40OTYgMTkuNjU2IDMuNDkgMTkuNjU2IDIuMjQ4IFogTSA5Ljg3MiAwIEwgMTQuMTkyIDAgTCA5LjQ1IDguOTkyIEwgNS4xMyA4Ljk5MiBaIE0gMTQuOTc0IDAgTCAxOS4yOTQgMCBMIDE1LjU5MiA3LjAyMSBDIDE1LjAxOCA4LjExIDEzLjU4NSA4Ljk5MiAxMi4zOTIgOC45OTIgTCAxMC4yMzIgOC45OTIgWiIgZmlsbD0icmdiKDAsIDAsIDApIj48L3BhdGg+Cjwvc3ZnPgo=&logoColor=white)|
| **Sass** | **스타일링** |![Sass](https://img.shields.io/badge/Sass-CC6699?style=flat-square&logo=Sass&logoColor=white)|
| **@hello-pangea/dnd** | **드래그 앤 드롭** |![npm](https://img.shields.io/badge/@hello--pangea/dnd-CB3837?style=flat-square&logo=npm&logoColor=white)|
| **react-date-range** | **날짜 범위 선택 라이브러리** |![npm](https://img.shields.io/badge/react--date--range-3d91ff?style=flat-square&logo=npm&logoColor=white)|
| **date-fns** | **날짜 및 시간 포맷, 계산** |![datefns](https://img.shields.io/badge/date--fns-770C56?style=flat-square&logo=datefns&logoColor=white)|

### 3. Back-End

| 사용기술 | 설명 | Badge |
| :---:| :---: | :---: |
| **Node.js** | **Express 서버의 기반** |![nodedotjs](https://img.shields.io/badge/Node.js-5FA04E?style=flat-square&logo=nodedotjs&logoColor=white)|
| **Express** | **Node.js 기반 웹 프레임워크** |![express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white)|
| **MongoDB** | **NoSQL 데이터베이스** |![mongodb](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)|
| **multer** | **파일 업로드 처리** |![npm](https://img.shields.io/badge/multer-CB3837?style=flat-square&logo=npm&logoColor=white)|
| **JSON** | **데이터 형식 / API 응답 처리, <br> MongoDB 데이터 저장 형식** |![JSON](https://img.shields.io/badge/JSON-000000?style=flat-square&logo=JSON&logoColor=white)|
| **Nodemon** | **개발 중 서버 자동 재시작 도구** |![nodemon](https://img.shields.io/badge/Nodemon-76D04B?style=flat-square&logo=nodemon&logoColor=white)|
| **Axios** | **서버에서 API 요청을 처리** |![axios](https://img.shields.io/badge/Axios-5A29E4?style=flat-square&logo=axios&logoColor=white)|

### 4. 개발 도구

|사용기술 | 설명 | Badge | 
| :---:| :---: | :---: |
| **Visual Studio Code (VS Code)** | **코드 편집기( 에디터 )** |![VSCode](https://img.shields.io/badge/VSCode-007ACC?style=flat-square&logo=data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMzIiIGhlaWdodD0iMzIiIHZpZXdCb3g9IjAgMCAzMiAzMiIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTI0LjAwMyAyTDEyIDEzLjMwM0w0Ljg0IDhMMiAxMEw4Ljc3MiAxNkwyIDIyTDQuODQgMjRMMTIgMTguNzAyTDI0LjAwMyAzMEwzMCAyNy4wODdWNC45MTNMMjQuMDAzIDJaTTI0IDkuNDM0VjIyLjU2NkwxNS4yODkgMTZMMjQgOS40MzRaIiBmaWxsPSJ3aGl0ZSIvPgo8L3N2Zz4K&logoColor=white) |
| **GitHub** | **버전 관리** |![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=GitHub&logoColor=white)| 
| **Postman** | **API 테스트** |![postman](https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white)|
| **Vercel** | **서버리스 플랫폼** |![vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)|
| **Figma** | **디자인 & UI/UX**|![Figma](https://img.shields.io/badge/Figma-F24E1E?style=flat-square&logo=Figma&logoColor=white) |

## 📚 참고 URL
- 화면 설계 : 
[떠나봅서 Figma](https://www.figma.com/design/4qzA0YnGtdHQzgfF2jcKhO/2%EC%B0%A8%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8_C%ED%8C%80---view?node-id=1-3153&t=ZuAkLG13SHbDVYt7-1)
- 발표 자료 : 
[떠나봅서 Canva](https://www.canva.com/design/DAGkzKa7pxo/1rKvlgXUlB83CsS5mzNg1A/view?utm_content=DAGkzKa7pxo&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=h25f34eab01)
- 인터페이스 기능 보고서
[떠나봅서 Interface Report](https://docs.google.com/document/d/1fuuSLIb9sE17m5Fwlu_JPVSAwZETH2YS544n9UcqkOM/edit?usp=sharing)
- 프로젝트 완료 보고서
[떠나봅서 Final report](https://drive.google.com/file/d/1p7JoSa3JEFsxeH1r3AOjASrCRa02txnF/view?usp=sharing)

<hr>

# 천지호의 개발 상세

## 📑 요약

### 담당 업무
- 개발 및 배포

### 담당 컴포넌트
- **MyMenu.jsx**: '마이페이지' 내 큰 메뉴 (체크리스트, 좋아요 등)
- **CmtItem.jsx**: '나의활동' 페이지 내 사용자가 작성한 댓글 리스트 아이템
- **CheckItem.jsx**: '체크리스트' 상세페이지 내 체크리스트 아이템 (MUI 플러그인 사용)
- **AddCheckItem.jsx**: '체크리스트' 상세페이지 내 추가용 input 아이템
- **Login (KakaoLogin.jsx, NaverLogin.jsx, GoogleLogin.jsx)**: 로그인 버튼, 클릭 시 각 소셜 플랫폼 로그인 요청

### 담당 페이지 목록
- [Splash (첫 방문 시)](https://jeju-trip-eosin.vercel.app/)
- [로그인](https://jeju-trip-eosin.vercel.app/login)
- [마이페이지 (자주묻는질문, 좋아요 제외)](https://jeju-trip-eosin.vercel.app/my)

## 🧩 공통 컴포넌트

1. **Popup** (`Btn1Popup.jsx`, `Btn2Popup.jsx`, `GetTripPopup.jsx`)  
   - 로그인, 로그아웃, 삭제 등 사용자 안내용 팝업  
   - 전달받은 타입에 따라 내용 표시 및 'onConfirm'으로 버튼 동작 관리

2. **Tab** (`TabItem.jsx`, `TabMenu.jsx`, `TabPage.jsx`)
   - TabMenu: 탭 선택 상태 표시 및 선택된 탭 인덱스 상위로 전달
   - TabPage: 타입별 탭 제목 및 메인 타이틀 설정  

3. **List** (`ListItem.jsx`, `ListPage.jsx`)  
   - ListPage: 데이터를 연도별 그룹화 및 최신순 정렬, 삭제 팝업 관리

## 💥 이슈 및 해결

### 1. Splash.jsx 렌더링 순서 문제  
- 메인 페이지가 먼저 보이고 Splash가 나중에 나타나는 현상  
- **해결**: App.js 렌더링 전에 조건문 추가, 최초 접속 시 Splash로 이동하고 방문 기록 저장, `replace` 사용해 히스토리 남기지 않음

### 2. Login.jsx
1. 카카오 토큰 요청 시 잘못된 파라미터 사용으로 인한 로그인 도중 400, 401 에러  
   - **해결**: 파라미터 이름은 개인이 설정하는 것이 아닌 카카오가 요구하는 key 이름 그대로 사용해야 하므로 수정(예: grant_type, client_id 등).

2. 소셜 로그인 정보를 저장하는 ‘provider’값이 제대로 저장되지 않아 로그아웃 방식에 혼란  
   - **해결**: 세션에 저장하는 코드를 KakaoLogin.jsx와 같은 인가 코드 요청 컴포넌트에 작성하여 위 컴포넌트들이 랜더링 될 때마다 실행. 하지만 실제 로그인이 이루어지는 건 버튼 클릭 후 페이지가 redirect 페이지로 바뀐 이후이기 때문에 이 코드는 로그인 시도 전에만 실행되고, 리다이렉트 되면 새로고침처럼 작동하여 세션이 초기화된 상태로 다시 시작되어 provider가 저장되지 않은 채 로그인. 따라서 로그인이 완료된 시점인 리다이렉트 페이지에서 사용자 정보를 저장할 때 provider를 함께 저장하는 방식으로 변경.

### 3. Logout.jsx - 로그아웃 팝업 및 이동 문제  
- 로그아웃 함수 비동기 처리로 팝업 및 페이지 이동 흐름 문제  
- **해결**: 팝업 띄우는 코드를 로그아웃 함수 내부 콜백으로 이동

### 4. ListPage.jsx - 스와이프된 아이템 복귀 문제  
- 삭제 취소 후에도 스와이프된 아이템이 제자리로 돌아가지 않음  
- **해결**: SwipeAction에 resetSwipe props 추가, 상태 초기화하여 아이템 원위치 복귀
