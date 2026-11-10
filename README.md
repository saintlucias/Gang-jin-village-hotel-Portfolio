<div align="center">

# 강진 마을호텔

### 하루쯤 머물고 싶은 병영 마을

**지역 관광 탐색 · 체험과 문화 프로그램 · 숙박 예약을 연결한 반응형 웹사이트**

**Next.js 15 · React 19 · TypeScript · SCSS Modules · Kakao Maps · Bootpay**

[원본 소스](https://github.com/saintlucias/Gang-jin-village-hotel-) · [주요 기능](#주요-기능) · [기술 스택](#기술-스택) · [인터랙션과-화면-효과](#인터랙션과-화면-효과) · [API 연동](#api-연동) · [화면 갤러리](#화면-갤러리)

</div>

![강진 마을호텔 메인 — 배너, 병영이야기, 관광지 안내](assets/screenshots/image.png)

## 프로젝트 소개

전라남도 강진군 병영면의 관광 정보와 도시재생사업을 소개하고, 체험·DIT 문화센터 프로그램·마을호텔 예약으로 이어지는 웹사이트를 구현했음.

방문자가 **지역 콘텐츠 탐색 → 상품 상세 확인 → 소셜 로그인 → 예약 → 예약 내역 확인** 순서로 이용할 수 있도록 화면과 외부 API를 연결했음. 관광지는 지도와 목록으로 탐색하고, 행사와 프로그램은 월간 캘린더에서도 확인할 수 있도록 구성했음.

이 저장소에는 프로젝트의 화면·기능·기술 구성을 소개하는 포트폴리오 README와 원본 저장소의 화면 자료를 정리했음. 구현 설명은 원본 소스의 [`62192f7`](https://github.com/saintlucias/Gang-jin-village-hotel-/commit/62192f7e4c79c3473d45708a874937b91e424da2) 커밋을 기준으로 작성했음.

## 구현 목표와 기대 효과

| 구현 목표 | 적용한 방법 | 기대 효과 |
| --- | --- | --- |
| 지역 정보와 예약 서비스의 연결 | 관광·체험·축제·시설 정보를 공통 메뉴와 상세 화면으로 연결했음 | 지역 정보를 확인한 뒤 예약 화면으로 이동할 수 있게 했음 |
| 장소 중심의 관광 탐색 | 카테고리 필터, 지도 마커, 장소 목록과 정보 패널을 구성했음 | 장소의 위치와 소개를 같은 화면에서 확인할 수 있게 했음 |
| 일정 중심의 이용 계획 | 월간 캘린더, 날짜별 일정, 숙박 기간 선택을 제공했음 | 방문 날짜에 맞춰 일정과 객실 정보를 확인할 수 있게 했음 |
| 다양한 기기의 화면 대응 | 데스크톱·태블릿·모바일 메뉴와 콘텐츠 배치를 구분했음 | 화면 너비에 맞는 탐색 방식과 카드 구성을 제공했음 |
| 예약 이후의 이용 관리 | 예약 종류별 내역, 상태별 취소·리뷰 버튼을 구성했음 | 신청 이후에도 예약 상태를 확인하고 후기를 남길 수 있게 했음 |

위 내용은 구현 의도와 기대 효과를 정리했으며, 방문자 수·예약 전환율·성능 개선율 등 측정되지 않은 운영 성과는 기재하지 않았음.

## 주요 기능

| 영역 | 구현 내용 |
| --- | --- |
| 메인 페이지 | 자동 배너, 병영이야기 카테고리, 체험 카드, 관광지 요약, 일정과 공지·보도자료를 배치했음 |
| 도시재생사업 | 도시재생 소개·뉴딜사업·마을관리 협동조합·성과 목록과 성과 상세 화면을 구성했음 |
| 병영이야기 | 카테고리별 목록, 페이지네이션, 유형별 상세 화면을 제공했음 |
| 관광지 정보 | 카테고리별 관광지 목록, 상세 소개, 이미지·영상 표시를 구현했음 |
| 2D 스마트지도 | Kakao Maps에 커스텀 마커를 표시하고 카테고리 필터·정보 패널·장소 목록을 연결했음 |
| 체험·DIT 프로그램 | 목록·상세·리뷰 조회, 최신순·일정 가까운 순·리뷰 많은 순 정렬, 예약 화면을 구성했음 |
| 축제·행사 | 행사 목록·상세와 메인 팝업을 제공하고 이미지에서 행사 상세로 이동하도록 연결했음 |
| 시설 안내 | 빈집살기 목록·상세, 마을호텔 목록·상세, DIT 문화센터 시설별 안내를 제공했음 |
| 숙박 날짜 선택 | 한국어 날짜 선택기에서 시작일·종료일을 지정하고 숙박일 수 표시와 객실 조회를 연결했음 |
| 예약 신청 | 상품 종류에 따라 체험·프로그램 신청과 호텔 결제 흐름을 분리하고 인원·연락처 입력을 구성했음 |
| 예약 확인·취소 | 체험·DIT 프로그램과 호텔을 탭으로 구분하고 이용정보·예약 상태·취소 요청을 제공했음 |
| 이용 후기 | 예약 상태에 따른 작성 진입, 텍스트 입력, 이미지 선택·미리보기·등록을 구현했음 |
| 소셜 로그인 | Google·Naver·Kakao 인증 이동, 콜백 처리, 사용자 상태 저장과 이전 화면 복귀를 연결했음 |
| 알림마당 | 공지사항·보도자료 검색과 페이지네이션, 상세·이전/다음 글, 첨부파일 다운로드를 구현했음 |
| 질문·문의 | 로그인 안내, 문의 목록·답변 표시, 제목·내용 입력과 문의 등록을 구성했음 |
| 캘린더 | 한국어 월간 일정, 종류별 색상 표시, 선택 날짜의 일정 목록과 전일·익일 이동을 제공했음 |
| 공통 사용성 | 전역 로딩 진행률, 오류 안내와 이동, 빈 목록 안내, 고정 캘린더 진입 버튼을 구성했음 |

## 주요 이용 흐름

```mermaid
flowchart LR
    A[메인·지역 콘텐츠] --> B[체험·프로그램·호텔 탐색]
    A --> C[스마트지도·캘린더]
    B --> D[상품 상세 확인]
    D --> E[소셜 로그인·예약 입력]
    E --> F[체험·프로그램 예약 API]
    E --> G[호텔 Bootpay 결제 요청]
    G --> H[영수증 ID를 포함한 호텔 예약 API]
    F --> I[예약 내역 확인]
    H --> I
    I --> J[상태에 따른 취소·리뷰 작성]
```

호텔 결제는 Bootpay의 `confirm` 이벤트에서 받은 `receipt_id`를 예약 정보와 함께 외부 API에 전송하도록 연결했음. 결제 승인·영수증 검증·환불의 서버 내부 구현과 실제 운영 결제 성공 여부는 이 프런트엔드 저장소만으로 확인할 수 없었음.

## 기술 스택

버전은 원본 `package-lock.json`에 고정된 설치 버전을 기준으로 정리했음.

| 구분 | 기술·버전 | 적용 내용 |
| --- | --- | --- |
| 웹 프레임워크 | Next.js `15.3.0` | `src/app` 기반 App Router, 공통 Layout, 동적 경로, 서버 측 API 요청 모듈을 사용했음 |
| UI | React·React DOM `19.1.0` | 함수형 컴포넌트와 Hooks를 사용하고 Context로 인증·로딩 상태를 공유했음 |
| 언어 | TypeScript `5.8.3` | `strict` 설정, 요청·응답 타입, 제네릭 페이지네이션·API 결과 타입을 적용했음 |
| 스타일 | Sass `1.86.3` · SCSS Modules | 컴포넌트별 스타일, 공통 색상·타이포그래피·믹스인, 반응형 미디어 쿼리를 구성했음 |
| 슬라이더 | Swiper `11.2.7` | 메인 자동 배너와 모바일·태블릿 콘텐츠의 가로 스와이프를 구현했음 |
| 지도 | Kakao Maps JavaScript SDK | 동적 SDK 로드, 좌표 기반 지도, CustomOverlay와 지도 중심 이동을 적용했음 |
| 일정표 | react-big-calendar `1.18.0` | 월간 일정과 사용자 정의 툴바, 날짜 선택·일정별 색상 표시를 구성했음 |
| 날짜 선택 | react-datepicker `8.3.0` | 숙박 기간 선택과 사용자 정의 날짜 입력 UI를 구현했음 |
| 날짜 처리 | date-fns `4.1.0` | 한국어 로케일, 월 범위·날짜 이동·숙박일 수 계산을 적용했음 |
| 결제 연동 | @bootpay/client-js `5.1.4` | KCP 카드 결제 요청과 이벤트별 콜백 처리를 연결했음 |
| 데이터 암호화 | crypto-js `4.2.0` · jsencrypt `3.3.2` | AES-CBC로 요청 본문을 암호화하고 RSA 공개키로 AES 키·IV를 암호화하는 흐름을 구현했음 |
| 식별자 | uuid `11.1.0` | 브라우저 세션 ID와 암호화 처리에 사용하는 임시 키·IV 문자열 생성에 사용했음 |
| 드래그 탐색 | react-use-draggable-scroll `0.4.7` | DIT 문화센터 이미지 목록의 드래그 스크롤을 구현했음 |
| 통신·파일 | Fetch API · FormData · Blob | 외부 API 요청, 리뷰 이미지 첨부, 게시글 첨부파일 다운로드를 구현했음 |
| 개발 도구 | Turbopack · ESLint 9 | 개발 서버의 `next dev --turbopack` 스크립트와 Next.js ESLint 설정을 구성했음 |
| 폰트·미디어 | Pretendard · Roboto · next/image · HTML video | 로컬 폰트, 이미지 표시, 영상 컨트롤과 이미지 확대 UI를 적용했음 |

Tailwind CSS `4.1.8`과 `react-textarea-autosize` `8.5.9`는 의존성에 등록되어 있으나, `src`에서 직접 사용되는 지점은 확인되지 않았음. 실제 화면 스타일은 SCSS Modules를 사용했고, 공통 입력창의 높이 조절은 `useLayoutEffect`와 `scrollHeight`로 구현했음.

## 인터랙션과 화면 효과

| 효과 | 구현 방식 | 사용자에게 제공하는 동작 |
| --- | --- | --- |
| 자동 배너 | Swiper의 `loop`, `centeredSlides`, `autoplay`를 적용했음 | 3초 간격으로 전환하고 이전·다음·일시정지·재생 버튼으로 제어할 수 있게 했음 |
| 기기별 슬라이드 | `useDevice`에 따라 배너 너비와 간격, 카드 레이아웃을 변경했음 | 작은 화면에서는 콘텐츠를 가로로 밀어 탐색할 수 있게 했음 |
| 내비게이션 전환 | 데스크톱의 마우스 진입 메뉴와 태블릿·모바일의 클릭 메뉴를 분리했음 | 화면과 입력 방식에 맞춰 하위 메뉴를 열 수 있게 했음 |
| 지도 툴팁·이동 | 마커의 마우스 진입·이탈 이벤트와 `panTo`를 사용했음 | 장소명을 미리 확인하고 선택한 장소로 지도를 이동할 수 있게 했음 |
| 지도 정보 패널 | 상세·간략 보기, 이전·다음 장소, 바깥 클릭 닫기를 구성했음 | 지도 위에서 장소 소개와 미디어를 확인할 수 있게 했음 |
| 이미지 확대 | 이미지 클릭 시 오버레이 모달을 표시했음 | 데스크톱·태블릿에서 상세 이미지를 확대하고 클릭으로 닫을 수 있게 했음 |
| 모바일 이미지 탐색 | 현재 이미지 인덱스와 이전·다음 버튼을 사용했음 | 여러 이미지를 한 장씩 순환해서 확인할 수 있게 했음 |
| 시설 이미지 드래그 | DIT 시설 목록에 `useDraggable` 이벤트를 연결했음 | 이미지 목록을 드래그하고 선택 시설의 안내를 확인할 수 있게 했음 |
| 부드러운 스크롤 | `scrollTo`·`scrollIntoView`의 `behavior: 'smooth'`를 적용했음 | 메인 상단과 캘린더의 날짜별 일정 영역으로 이동할 수 있게 했음 |
| 카드·버튼 피드백 | SCSS의 `:hover`와 그림자·색상·불투명도 전환을 사용했음 | 카드·버튼의 상호작용 상태를 시각적으로 구분했음 |
| 로딩 진행률 | 요청 시작·완료 수를 Context로 계산하고 진행 막대 너비를 전환했음 | 여러 데이터 요청의 진행 상황을 공통 UI로 표시했음 |
| 행사 팝업 숨김 | `localStorage`에 당일 종료 시각을 저장했음 | ‘오늘 하루 보지 않기’를 선택하면 해당 날짜의 재노출을 제한했음 |

반응형 분기는 **데스크톱 1280px 이상, 태블릿 840~1279px, 모바일 839px 이하**로 구성했음.

## 구조와 설계

```text
src/
├── app/                     # 페이지·공통 레이아웃·전역 스타일
│   ├── City-Regeneration/   # 도시재생 소개·성과
│   ├── Tour/                # 지도·이야기·관광지
│   ├── Event/               # 체험·축제
│   ├── Builder/             # 빈집살기·호텔·DIT
│   ├── Reservation/         # 예약 상세·신청
│   ├── Confirm-Reservation/ # 예약 내역·후기 작성
│   ├── Notification/        # 공지·보도자료·문의
│   ├── Calendars/           # 월간·날짜별 일정
│   ├── Login/               # 로그인·소셜 콜백
│   └── Error/               # 오류 안내
├── components/
│   ├── basic/               # 버튼·아이콘·입력·이미지 모달
│   ├── expansion/           # 탭·검색·날짜 선택 등 조합 UI
│   └── module/              # 도메인별 화면 모듈
├── api/                     # API_Main.ts·network.ts
├── context/                 # 인증·전역 로딩
├── hooks/                   # 기기·세션·검증·결제·암호화
├── types/                   # 공통·요청·응답 타입
├── constants/               # 메뉴·필터·오류·검증·리소스 상수
├── styles/                  # SCSS Modules·디자인 토큰
└── utils/                   # 미디어 경로·이동 보조 함수
```

### 화면·API 책임 분리

화면 컴포넌트에서 `API_Main.ts`의 도메인 함수를 호출하고, 해당 함수가 검색·페이지·날짜 조건과 세션 정보를 준비하도록 구성했음. `'use server'`가 선언된 `network.ts`에서는 외부 서버로 Fetch 요청을 보내고 HTTP 응답을 공통 결과 타입으로 변환했음.

`Action_Response<T>`는 API 본문의 `result`를 확인해 성공 콜백과 오류 콜백을 분기했음. `PageNationData<T>`와 요청·응답 인터페이스를 공통으로 사용해 목록·상세 데이터의 구조를 명시했음.

### 인증·세션 관리

`UserAuth` Context로 사용자 상태와 로그인·로그아웃 동작을 공유하고, `sessionStorage`에 사용자 정보·UUID 세션 ID·복귀 경로·숙박 날짜를 저장했음. 소셜 로그인 콜백에서 `code`와 `state`를 읽어 외부 로그인 API에 전달한 뒤, 저장된 이전 화면으로 복귀하도록 연결했음.

### 입력·상태 처리

공통 검증 Hook에 문의 제목·내용, 후기 내용, 예약 식별자·전화번호 규칙을 전달하도록 구성했음. 인원 선택은 1명부터 상품별 제한 인원까지 조절하고, 예약 상태에 따라 취소·리뷰 작성 버튼의 사용 가능 여부를 구분했음. 리뷰 이미지는 JPG·JPEG·PNG와 5MB 이하 조건을 확인하고 선택 직후 미리보기를 표시했음.

## API 연동

### 외부 서비스

| 서비스 | 연결 방식 | 구현 범위 |
| --- | --- | --- |
| Kakao Maps | `dapi.kakao.com/v2/maps/sdk.js` | 지도 SDK 로드, 좌표·커스텀 마커·장소 정보 표시를 구현했음 |
| Google 로그인 | `accounts.google.com/o/oauth2/v2/auth` | 인증 코드 요청과 공통 콜백·외부 로그인 API 연결을 구현했음 |
| Naver 로그인 | `nid.naver.com/oauth2.0/authorize` | 인증 코드 요청과 공통 콜백·외부 로그인 API 연결을 구현했음 |
| Kakao 로그인 | `kauth.kakao.com/oauth/authorize` | 인증 코드 요청과 공통 콜백·외부 로그인 API 연결을 구현했음 |
| Bootpay | `@bootpay/client-js` | KCP 카드 결제 요청, `confirm` 이벤트의 영수증 ID 전달과 결제창 종료 처리를 구현했음 |
| 콘텐츠·예약 서버 | 서버 측 Fetch | 관광·시설·게시판·일정 조회와 로그인·예약·취소·리뷰 등록을 연동했음 |

### 도메인별 API

실제 서버 URL과 API 경로는 환경변수로 조합하도록 구현되어 있어, 아래에는 코드에 정의된 **환경변수 식별자와 HTTP 메서드**를 정리했음. 접두사 `NEXT_PUBLIC_`는 표의 가독성을 위해 생략했음.

| 도메인 | 메서드 | 경로 환경변수 | 요청·응답 용도 |
| --- | --- | --- | --- |
| 암호화 정보 | GET | `ENCRYPTION` | 서버 공개키와 `networkId`를 요청했음 |
| 병영이야기 | GET | `CBMS_STORY_CATEGORY_LIST`, `CBMS_STORY_LIST`, `CBMS_STORY` | 카테고리·목록·상세를 조회했음 |
| 관광지·지도 | GET | `CBMS_TOUR_LIST`, `CBMS_CATEGORY`, `CBMS_MARKER_LIST`, `CBMS_MARKER` | 관광 요약·카테고리·장소 목록·상세를 조회했음 |
| 체험 | GET | `CBMS_ACTIVITY_LIST`, `CBMS_ACTIVITY` | 체험 목록과 상세를 조회했음 |
| 축제·행사 | GET | `CBMS_FESTIVAL_LIST`, `CBMS_FESTIVAL` | 행사 목록과 상세를 조회했음 |
| 빈집살기 | GET | `CBMS_SHARE_HOUSE_LIST`, `CBMS_SHARE_HOUSE` | 시설 목록과 상세를 조회했음 |
| DIT 문화센터 | GET | `CBMS_DIT_LIST` | 시설 안내 데이터를 조회했음 |
| 마을호텔 | GET | `HOTEL_LIST`, `HOTEL` | 숙박 날짜 조건을 포함한 객실 목록과 상세를 조회했음 |
| 공지·보도자료 | GET | `CBMS_NOTICE_LIST`, `CBMS_NOTICE`, `CBMS_NEWS_LIST`, `CBMS_NEWS` | 검색·목록·상세 데이터를 조회했음 |
| 질문·문의 | GET / POST | `QNA_LIST` / `REQUEST_QNA` | 문의 목록·답변을 조회하고 암호화한 문의 내용을 등록했음 |
| 소셜 로그인 | POST | `SOCIAL_LOGIN` | 인증 코드와 플랫폼 코드로 사용자 정보를 요청했음 |
| 체험·프로그램 예약 | POST | `RESERVATION` | 상품 ID·인원·연락처를 포함한 예약 요청을 전송했음 |
| 체험·프로그램 내역 | GET / DELETE | `RESERVATION_LIST` | 예약 내역 조회와 예약 취소 요청을 전송했음 |
| 호텔 예약 | POST | `HOTEL_RESERVATION` | 호텔 ID·영수증 ID·숙박 기간·인원·연락처를 전송했음 |
| 호텔 예약 내역 | GET / DELETE | `HOTEL_RESERVATION_LIST` | 호텔 예약 내역 조회와 취소 요청을 전송했음 |
| 후기 | GET / POST | `ACTIVITY_REVIEW_LIST` / `ACTIVITY_REVIEW_REGISTER` | 후기 목록을 조회하고 텍스트·이미지를 등록했음 |
| 일정·팝업 | GET | `CALENDAR`, `POPUP_LIST` | 기간별 일정과 메인 행사 팝업을 조회했음 |
| 도시재생 성과 | GET | `CITYREGENERATION_LIST`, `CITYREGENERATION` | 성과 목록과 상세를 조회했음 |

공통 요청은 `NEXT_PUBLIC_MASTER_KEY`를 서버 기준 주소로 사용하고, `sessionId` 헤더를 전달하도록 구성했음. 목록 요청에는 `currentPage`, `pageSize`와 필요에 따른 `categoryFilter`, `sort`, `search`, `startTime`, `endTime` 조건을 사용했음.

문의·예약·취소·후기 등록 흐름에서는 서버 공개키를 조회한 뒤 본문을 AES로 암호화하고, RSA로 암호화한 키·IV와 `networkId`를 헤더에 전달하도록 구현했음. 후기 등록은 암호화된 텍스트와 이미지 파일을 `FormData`에 담아 전송했음. 이는 소스에서 확인한 요청 처리 구조이며 보안 검증 결과를 의미하지 않음.

## 페이지 구성

| 화면 | 경로 | 화면 역할 |
| --- | --- | --- |
| 메인 | `/` | 지역 콘텐츠·예약 서비스의 진입 화면으로 구성했음 |
| 도시재생 | `/City-Regeneration/intro`, `/newdeal`, `/village-cooperative`, `/achievement` | 모두 `/City-Regeneration` 하위 경로이며 사업 소개와 성과를 제공했음 |
| 도시재생 성과 상세 | `/City-Regeneration/achievement/[id]` | 개별 성과를 확인하도록 구성했음 |
| 스마트지도 | `/Tour/Map` | 지도에서 관광지를 탐색하도록 구성했음 |
| 병영이야기 | `/Tour/Story`, `/Tour/Story/A/[id]`, `/Tour/Story/B/[id]` | 목록과 유형별 상세를 제공했음 |
| 관광지 | `/Tour/Marker`, `/Tour/Marker/[id]` | 목록과 장소 상세를 제공했음 |
| 체험·축제 | `/Event/Activity`, `/Event/Festival`, `/Event/Festival/[id]` | 상품·행사 목록과 축제 상세를 제공했음 |
| 빈집살기·호텔 | `/Builder/ShareHouse`, `/Builder/Hotel`, 각 경로의 `/[id]` | 시설 목록과 상세를 제공했음 |
| DIT 문화센터 | `/Builder/DIT`, `/Builder/DIT/Program` | 문화센터 안내와 프로그램 목록을 제공했음 |
| 예약 | `/Reservation/[category]/[id]`, `/Reservation/Excute/[category]/[id]` | 체험·프로그램 상세와 상품 종류별 신청을 제공했음 |
| 예약 확인·후기 | `/Confirm-Reservation`, `/Confirm-Reservation/review/[resUserId]` | 이용 내역 확인과 후기 작성을 제공했음 |
| 알림마당 | `/Notification/Notice`, `/Notification/News`, 각 경로의 `/[id]` | 게시판 목록·검색·상세를 제공했음 |
| 문의 | `/Notification/QnA`, `/Notification/QnA/Write` | 문의 조회와 작성을 제공했음 |
| 일정·인증·오류 | `/Calendars`, `/Login`, `/Login/social`, `/Error/[code]` | 공통 일정·인증·오류 처리 화면을 제공했음 |

## 화면 갤러리

원본 README에 포함된 화면 자료 39개를 함께 정리했음. 아래 이미지는 원본 저장소에 기록된 화면 자료를 재사용했음.

### 스마트지도

![2D 스마트지도 — 카테고리 필터, 커스텀 마커, 장소 정보와 목록](assets/screenshots/image-11.png)

### 마을호텔과 예약

![마을호텔 목록 — 숙박 날짜 선택과 객실 탐색](assets/screenshots/image-19.png)

<details>
<summary>호텔 상세·예약 입력·예약 확인</summary>

![마을호텔 상세](assets/screenshots/image-34.png)
![마을호텔 예약 입력](assets/screenshots/image-35.png)
![예약 확인](assets/screenshots/image-26.png)

</details>

### 캘린더

![월간 캘린더](assets/screenshots/image-27.png)

<details>
<summary>날짜별 일정</summary>

![선택 날짜의 일정 목록](assets/screenshots/image-28.png)

</details>

<details>
<summary>메인 페이지 추가 화면</summary>

![메인 콘텐츠](assets/screenshots/image-1.png)
![메인 일정과 알림](assets/screenshots/image-2.png)

</details>

<details>
<summary>도시재생사업 — 소개·뉴딜·협동조합·성과</summary>

![도시재생 소개 1](assets/screenshots/image-3.png)
![도시재생 소개 2](assets/screenshots/image-4.png)
![도시재생 소개 3](assets/screenshots/image-5.png)
![뉴딜사업 1](assets/screenshots/image-6.png)
![뉴딜사업 2](assets/screenshots/image-7.png)
![마을관리 협동조합 1](assets/screenshots/image-8.png)
![마을관리 협동조합 2](assets/screenshots/image-9.png)
![도시재생 성과](assets/screenshots/image-10.png)

</details>

<details>
<summary>병영이야기·관광지 — 목록과 상세</summary>

![병영이야기 목록 1](assets/screenshots/image-12.png)
![병영이야기 목록 2](assets/screenshots/image-13.png)
![병영이야기 상세](assets/screenshots/image-29.png)
![관광지 목록 1](assets/screenshots/image-14.png)
![관광지 목록 2](assets/screenshots/image-15.png)
![관광지 상세](assets/screenshots/image-30.png)

</details>

<details>
<summary>체험·축제 — 목록과 상세</summary>

![체험 목록](assets/screenshots/image-16.png)
![체험 상세](assets/screenshots/image-31.png)
![축제와 행사 목록](assets/screenshots/image-17.png)
![축제와 행사 상세](assets/screenshots/image-32.png)

</details>

<details>
<summary>빈집살기·DIT 문화센터 — 시설·프로그램·후기</summary>

![빈집살기 목록](assets/screenshots/image-18.png)
![빈집살기 상세](assets/screenshots/image-33.png)
![DIT 문화센터 소개](assets/screenshots/image-20.png)
![DIT 프로그램 목록](assets/screenshots/image-21.png)
![DIT 프로그램 상세와 후기](assets/screenshots/image-36.png)

</details>

<details>
<summary>알림마당 — 공지·보도자료·문의</summary>

![공지사항 목록](assets/screenshots/image-22.png)
![공지사항 상세](assets/screenshots/image-37.png)
![보도자료 목록](assets/screenshots/image-23.png)
![보도자료 상세](assets/screenshots/image-38.png)
![질문과 문의 목록](assets/screenshots/image-24.png)
![문의 작성](assets/screenshots/image-25.png)

</details>

## 원본 실행 안내

아래 명령은 실행 코드가 있는 **원본 저장소**를 기준으로 정리했음. 이 포트폴리오 저장소에는 실행 앱을 포함하지 않았음.

```bash
git clone https://github.com/saintlucias/Gang-jin-village-hotel-.git
cd Gang-jin-village-hotel-
npm ci
npm run dev
```

실행 전 원본 루트의 `.env.local`에 서버 주소·도메인별 API 경로·Kakao 지도 키·소셜 로그인 클라이언트 ID·기준 URL·리다이렉트 경로를 설정하도록 구성되어 있음. 환경변수 이름은 `src/api/network.ts`, `src/context/UserAuth.tsx`, `src/components/module/map/mapView.tsx`에서 확인할 수 있으며 실제 값과 외부 서버는 별도로 준비해야 함을 확인했음.

`npm run build`와 `npm run start`는 각각 프로덕션 빌드와 실행 스크립트로 정의되어 있음. 이번 작업은 원본 코드·설정·화면 자료 분석을 대상으로 했으며, 외부 API·소셜 인증·지도·실결제의 실행 검증은 수행하지 않았음.

## 구현 근거

아래 링크는 분석한 커밋의 파일을 가리키도록 고정했음.

| 확인 항목 | 원본 소스 |
| --- | --- |
| 의존성·설치 버전 | [package.json][source-package] · [package-lock.json][source-lock] |
| 라우팅·공통 화면 | [src/app][source-app] · [layout.tsx][source-layout] |
| 통신·도메인 API | [network.ts][source-network] · [API_Main.ts][source-api] |
| 인증·복귀 경로 | [UserAuth.tsx][source-auth] · [social_login.tsx][source-social] |
| 지도·장소 탐색 | [mapView.tsx][source-map] |
| 캘린더·날짜 선택 | [CalendarView.tsx][source-calendar] · [dateSelectPicker.tsx][source-datepicker] |
| 결제·예약 입력 | [useBootPay.ts][source-payment] · [res_excute_view.tsx][source-reservation] |
| 암호화·공통 로딩 | [useEncryption.ts][source-encryption] · [LoadingProvider.tsx][source-loading] |
| 화면 효과·반응형 | [Banner.tsx][source-banner] · [useDevice.ts][source-device] · [styles][source-styles] |
| 이미지 후기·파일 처리 | [cr_review.tsx][source-review] · [load_url.tsx][source-download] |
| 화면 자료 | [원본 README][source-readme] · [readme 이미지 폴더][source-screens] |

[source-package]: https://github.com/saintlucias/Gang-jin-village-hotel-/blob/62192f7e4c79c3473d45708a874937b91e424da2/package.json
[source-lock]: https://github.com/saintlucias/Gang-jin-village-hotel-/blob/62192f7e4c79c3473d45708a874937b91e424da2/package-lock.json
[source-app]: https://github.com/saintlucias/Gang-jin-village-hotel-/tree/62192f7e4c79c3473d45708a874937b91e424da2/src/app
[source-layout]: https://github.com/saintlucias/Gang-jin-village-hotel-/blob/62192f7e4c79c3473d45708a874937b91e424da2/src/app/layout.tsx
[source-network]: https://github.com/saintlucias/Gang-jin-village-hotel-/blob/62192f7e4c79c3473d45708a874937b91e424da2/src/api/network.ts
[source-api]: https://github.com/saintlucias/Gang-jin-village-hotel-/blob/62192f7e4c79c3473d45708a874937b91e424da2/src/api/API_Main.ts
[source-auth]: https://github.com/saintlucias/Gang-jin-village-hotel-/blob/62192f7e4c79c3473d45708a874937b91e424da2/src/context/UserAuth.tsx
[source-social]: https://github.com/saintlucias/Gang-jin-village-hotel-/blob/62192f7e4c79c3473d45708a874937b91e424da2/src/components/module/Login/social_login.tsx
[source-map]: https://github.com/saintlucias/Gang-jin-village-hotel-/blob/62192f7e4c79c3473d45708a874937b91e424da2/src/components/module/map/mapView.tsx
[source-calendar]: https://github.com/saintlucias/Gang-jin-village-hotel-/blob/62192f7e4c79c3473d45708a874937b91e424da2/src/components/module/Calendar/CalendarView.tsx
[source-datepicker]: https://github.com/saintlucias/Gang-jin-village-hotel-/blob/62192f7e4c79c3473d45708a874937b91e424da2/src/components/expansion/dateSelectPicker.tsx
[source-payment]: https://github.com/saintlucias/Gang-jin-village-hotel-/blob/62192f7e4c79c3473d45708a874937b91e424da2/src/hooks/useBootPay.ts
[source-reservation]: https://github.com/saintlucias/Gang-jin-village-hotel-/blob/62192f7e4c79c3473d45708a874937b91e424da2/src/components/module/Reservation/res_excute_view.tsx
[source-encryption]: https://github.com/saintlucias/Gang-jin-village-hotel-/blob/62192f7e4c79c3473d45708a874937b91e424da2/src/hooks/useEncryption.ts
[source-loading]: https://github.com/saintlucias/Gang-jin-village-hotel-/blob/62192f7e4c79c3473d45708a874937b91e424da2/src/context/LoadingProvider.tsx
[source-banner]: https://github.com/saintlucias/Gang-jin-village-hotel-/blob/62192f7e4c79c3473d45708a874937b91e424da2/src/components/module/banner/Banner.tsx
[source-device]: https://github.com/saintlucias/Gang-jin-village-hotel-/blob/62192f7e4c79c3473d45708a874937b91e424da2/src/hooks/useDevice.ts
[source-styles]: https://github.com/saintlucias/Gang-jin-village-hotel-/tree/62192f7e4c79c3473d45708a874937b91e424da2/src/styles
[source-review]: https://github.com/saintlucias/Gang-jin-village-hotel-/blob/62192f7e4c79c3473d45708a874937b91e424da2/src/components/module/Confirm-Reservation/cr_review.tsx
[source-download]: https://github.com/saintlucias/Gang-jin-village-hotel-/blob/62192f7e4c79c3473d45708a874937b91e424da2/src/components/module/Notification/load_url.tsx
[source-readme]: https://github.com/saintlucias/Gang-jin-village-hotel-/blob/62192f7e4c79c3473d45708a874937b91e424da2/README.md
[source-screens]: https://github.com/saintlucias/Gang-jin-village-hotel-/tree/62192f7e4c79c3473d45708a874937b91e424da2/readme
