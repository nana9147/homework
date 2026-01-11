# 마크다운 문법

## 1. HTML이란?

웹 페이지의 구조와 의미를 정의하는 마크업 언어  
 브라우저는 HTML 문서를 DOM 트리 구조로 변환하여 렌더링함

### ✔️ DOM 트리

- HTML 문서를 트리 구조로 변환한 결과
- CSS, JavaScript는 DOM 기준으로 동작

## 2. 문서 기본 구조

브라우저, 검색엔진, 접근성 도구가 이 구조를 기준으로 문서 해석

```html
<!DOCTYPE html>
<html lang="ko">
  <head></head>
  <body></body>
</html>
```

## 3. DOCTYPE

브라우저에게 HTML5 문서임을 알리는 선언  
선언하지 않으면 Quirks Mode(구버전 호환 모드) 로 렌더링될 수 있음

## 4. 기본 태그

`<html>` 문서 전체를 감싸는 최상위 요소
`<head>` 메타데이터, 스타일, 스크립트
`<body>` 사용자에게 보여지는 콘텐츠

## 5. head 태그 (메타데이터)

사용자에게는 보이지 않지만 문서 정보 정의

```html
<head>
  <meta charset="UTF-8" />
  <title>문서 제목</title>
  <meta name="description" content="페이지 설명" />
</head>
```

### ✔️ 요소

- `<meta charset>` 문자 인코딩
- `<title>` 브라우저 탭 제목
- `<meta name>` 검색엔진, 문서 정보

## 6. 시맨틱 태그

의미 중심의 구조 제공  
SEO, 접근성, 유지보수성 향상

### ✔️ 태그

`<header>` 상단 영역
`<nav>` 내비게이션
`<main>` 핵심 콘텐츠
`<section>` 주제별 구역
`<article>` 독립 콘텐츠
`<aside>` 보조 콘텐츠
`<footer>` 하단 영역

⭐ 목적: 구조를 명확히 표현

## 7. 텍스트 관련 태그

- `<h1>~<h6>` 제목
- `<p>` 문단
- `<br />` 줄바꿈
- `<hr />` 구분선

## 8. 강조 태그

- `<strong>` 중요 강조
- `<em>` 의미적 강조
- `<del>` 삭제된 내용

## 9. 목록 태그

a. 순서 없는 목록

```html
<ul>
  <li>항목</li>
</ul>
```

b. 순서 있는 목록

```html
<ol>
  <li>항목</li>
</ol>
```

## 10. 링크와 이미지

- `<a>` 하이퍼링크
- `<img />` 이미지

## 11. 미디어 태그

- `<video>` 비디오
- `<audio>` 오디오

## 12. 테이블 태그

```html
<table>
  <thead>
    <tr>
      <th>제목</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>내용</td>
    </tr>
  </tbody>
</table>
```

## 13. 폼(Form) 태그

사용자 입력 처리

- `<form>` 입력 영역
- `<input>` 입력 필드
- `<textarea>` 여러 줄 입력
- `<button>` 버튼
- `<label>` 입력 설명

## 14. 블록 / 인라인 요소

- 블록 -> 한 줄 전체 차지 (div, p)
- 인라인 -> 내용만 차지 (span, a)

## 15. 전역 속성

모든 HTML 태그에서 공통으로 사용할 수 있는 속성  
\* CSS·JavaScript와의 연계를 위해 필수

### ✔️ 주요 전역 속성

- id - 문서 내에서 고유한 식별자
- class - 스타일 및 스크립트 적용을 위한 그룹
- style - 인라인 스타일 지정
- title - 마우스 오버 시 툴팁 표시
- data-\* - 사용자 정의 데이터 저장
- hidden - 화면에서 요소 숨김

## 16. 비시맨틱 레이아웃 태그

의미는 없지만 레이아웃 구성에 사용되는 기본 컨테이너

- `<div>` 의미 없는 블록 요소 (레이아웃 용도)
- `<span>` 의미 없는 인라인 요소 (텍스트 일부 제어)

## 17. 접근성(Accessibility) 관련 속성

스크린 리더, 보조 기기를 위한 정보 제공  
HTML 시맨틱 구조를 완성하는 요소

### ✔️ 주요 속성

- alt - 이미지 대체 텍스트
- aria-label - 요소 설명 제공
- aria-hidden - 접근성 도구에서 숨김

## 18. 외부 콘텐츠 삽입 (iframe)

다른 웹 페이지나 외부 리소스를 문서에 포함

```html
<iframe src="https://example.com"></iframe>
```

\* 지도, 영상, 외부 페이지 임베드 시 사용

## 19. 외부 리소스 연결 태그

HTML과 CSS, JavaScript를 연결

### ✔️ 태그

- `<link>` 외부 CSS 파일 연결
- `<script>` JavaScript 파일 로드 및 실행

## 20. 메타 태그 확장 (반응형 웹)

모바일 환경 대응을 위한 필수 설정

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

- 화면 너비를 기기 기준으로 설정
- 반응형 레이아웃의 기준점

## 21. HTML 엔티티(Entity)

HTML에서 예약된 문자를 문자 그대로 표현하기 위한 표기법

### ✔️ 주요 엔티티

- `&lt;` → <
- `&gt;` → >
- `&amp;` → &
- `&nbsp;` -> 공백
