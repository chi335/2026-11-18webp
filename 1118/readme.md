# 🌐 Web Programming & Front-End Core Study Notes

> 웹 개발 환경 구축(바이브 코딩 등)부터 **HTML5 시맨틱 구조 설계, CSS3 스타일 규칙 및 레이아웃, JavaScript와 브라우저 엔진 동작 원리, HTML5 Canvas 2D 그래픽스 프로그래밍**
---

## 📌 목차 (Table of Contents)
1. [01. 바이브 코딩 입문과 환경 준비](#1-01-바이브-코딩-입문과-환경-준비)
2. [02. HTML 구조와 정보 설계](#2-02-html-구조와-정보-설계)
3. [03. CSS 기본과 스타일 규칙 및 예제](#3-03-css-기본과-스타일-규칙-및-예제)
4. [04. JavaScript와 브라우저의 역할](#4-04-javascript와-브라우저의-역할)
5. [11. HTML5 캔버스 그래픽 (Canvas API)](#5-11-html5-캔버스-그래픽-canvas-api)

---

## 1. 01. 바이브 코딩 입문과 환경 준비

현대적인 웹 개발 트렌드(AI 어시스턴트 기반 바이브 코딩), 웹 기본 생태계, 개발 환경 구축 및 웹 표준/접근성을 다룹니다.

### 💡 핵심 정리
* **바이브 코딩 (Vibe Coding)**:
  * 생성형 AI 어시스턴트(Copilot, ChatGPT 등)를 활용하여 빠른 프로토타이핑과 구현 속도를 극대화하는 코딩 방식.
  * 기초 웹 기술(HTML/CSS/JS) 원리를 명확히 이해해야 AI 생성 코드를 검증하고 최적화 가능.
* **웹 개발 3대 요소 역할 분담**:
  * **HTML (HyperText Markup Language)**: 웹 문서의 뼈대 구조 및 데이터 전달
  * **CSS (Cascading Style Sheets)**: 비주얼 스타일링, 레이아웃 및 디자인 표현
  * **JavaScript**: 웹 문서의 동적 제어, 비동기 통신(AJAX/Fetch) 및 사용자 인터랙션
* **개발 환경 (Environment & Tools)**:
  * **IDE/Editor**: Visual Studio Code (VS Code)
  * **핵심 Extension**: Live Server (로컬 서버 환경), Prettier (코드 포맷팅), ESLint (문법 검사)
  * **Debugging Tool**: Chrome DevTools (Elements, Console, Network, Application 탭 활용)
* **웹 표준(Web Standards) & 웹 접근성(A11y)**:
  * W3C 표준 규격 준수 ➔ 크로스 브라우징(Cross-Browsing) 보장
  * 반응형 웹 디바이스 대응 (`<meta name="viewport" content="width=device-width, initial-scale=1.0">`)

---

## 2. 02. HTML 구조와 정보 설계

웹 문서의 시맨틱(Semantic) 정보 설계와 검색 엔진 최적화(SEO), 사용자 입력을 받는 Form 요소의 구성을 정리합니다.

### 💡 핵심 정리
* **HTML5 표준 문서 구조**:
  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML 정보 설계</title>
  </head>
  <body>
    <!-- 사용자에게 시각적으로 보여지는 영역 -->
  </body>
  </html>
  ```
* **시맨틱 태그 (Semantic Tags)**:
  * 단순 구획 분리가 아닌 **의미(Meaning)**를 태그에 부여함으로써 SEO 및 스크린 리더 접근성 제고.
  * `<header>`: 상단 영역 (로고, 메인 메뉴)
  * `<nav>`: 네비게이션 메뉴 바
  * `<main>`: 문서의 핵심 유일 콘텐츠
  * `<section>`: 주제별 단락 구획
  * `<article>`: 독립적으로 유통 가능한 컨텐츠 (포스트, 뉴스 기사)
  * `<aside>`: 사이드바, 광고 등 부가 정보
  * `<footer>`: 하단 저작권, 연락처 정보
* **폼(Form) 설계 및 데이터 수집**:
  * 사용자 데이터를 백엔드로 제출하기 위한 통로 (`<form action="..." method="POST">`)
  * `<input type="text|email|password|checkbox|radio">`, `<select>`, `<textarea>`, `<button>`
  * 유효성 검사 속성: `required`, `pattern`, `placeholder`, `value`, `name`

---

## 3. 03. CSS 기본과 스타일 규칙 및 예제

웹 디자인 구현을 위한 CSS 스타일 규칙, 박스 모델(Box Model), Flexbox 및 Grid 레이아웃 기법을 정리합니다.

### 💡 핵심 정리
* **CSS 적용 3가지 방식**:
  1. Inline (`style="..."`) - 유지보수에 비효율적
  2. Internal (`<style>` 태그)
  3. External (`<link rel="stylesheet" href="style.css">`) - 모듈화 및 캐싱에 최적화
* **선택자(Selectors) 및 우선순위 (Specificity)**:
  * `*` (전체) < `태그` < `.클래스` < `#ID` < Inline Style < `!important`
  * 가상 클래스/요소: `:hover`, `:focus`, `:nth-child()`, `::before`, `::after`
* **박스 모델 (Box Model)**:
  * `Margin` ➔ `Border` ➔ `Padding` ➔ `Content`
  * Layout 계산 왜곡을 방지하기 위해 `box-sizing: border-box;` 필수 사용.
* **레이아웃(Layout) 핵심 시스템**:
  * **Flexbox (1D 시스템)**: `display: flex`, `flex-direction`, `justify-content` (주축 정렬), `align-items` (교차축 정렬)
  * **Grid (2D 시스템)**: `display: grid`, `grid-template-columns`, `gap`
  * **Positioning**: `static`, `relative`, `absolute`, `fixed`, `sticky`

```css
/* 글로벌 전역 초기화 및 카드 레이아웃 예시 */
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

.card-wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 20px;
  max-width: 1200px;
  margin: 0 auto;
}
```

---

## 4. 04. JavaScript와 브라우저의 역할

자바스크립트 언어 기본, 브라우저 렌더링 파이프라인의 이해 및 DOM/BOM 기반 이벤트 동적 제어를 정리합니다.

### 💡 핵심 정리
* **브라우저 렌더링 파이프라인 (Critical Rendering Path)**:
  1. **Parsing**: HTML/CSS 파싱 ➔ DOM Tree & CSSOM Tree 생성
  2. **Render Tree**: 화면에 보일 노드만으로 구성된 Render Tree 구축
  3. **Layout (Reflow)**: 각 노드의 위치와 크기(픽셀) 계산
  4. **Paint (Repaint)**: 화면 픽셀에 색상 및 이미지를 그려넣음
* **DOM (Document Object Model) 다루기**:
  * HTML 요소를 자바스크립트 객체로 노드화하여 조작.
  * `document.querySelector()`, `document.querySelectorAll()`
  * `element.textContent`, `element.classList.toggle()`, `element.appendChild()`
* **이벤트 흐름 및 이벤트 위임**:
  * **이벤트 전달 3단계**: Capturing ➔ Target ➔ Bubbling
  * **이벤트 위임 (Event Delegation)**: 부모 요소에 하나의 이벤트 리스너를 등록하여 동적으로 생성되는 자식 요소의 이벤트를 일괄 처리.

```javascript
// DOM 조작 및 이벤트 위임 예제
const todoList = document.querySelector("#todo-list");

// 부모 요소에 이벤트 위임 처리
todoList.addEventListener("click", (event) => {
  if (event.target.classList.contains("delete-btn")) {
    const item = event.target.closest("li");
    item.remove();
  }
});
```

---

## 5. 11. HTML5 캔버스 그래픽 (Canvas API)

별도의 플러그인(Flash 등) 없이 자바스크립트로 브라우저 상에 2D 그래픽, 도형, 텍스트, 이미지를 실시간 렌더링하는 API입니다.

### 💡 핵심 정리
* **`<canvas>` 태그 및 렌더링 컨텍스트 (Context)**:
  * 웹 페이지 내 Graphic Drawing 영역 확보 (`width`, `height` 기본값: 300x150 픽셀).
  * `canvas.getContext("2d")` 객체를 통해 그리기 도구(Context) 호출.
* **경로(Path) 기반 도형 그리기**:
  * `beginPath()`: 경로 초기화
  * `moveTo(x, y)`: 시작 좌표 설정
  * `lineTo(x, y)`: 직선 경로 추가
  * `rect(x, y, width, height)` / `strokeRect()` / `fillRect()`: 사각형
  * `arc(x, y, radius, startAngle, endAngle, counterclockwise)`: 원호 및 원
  * `stroke()`: 경로 외곽선 렌더링
  * `fill()`: 경로 내부 채우기 렌더링
  * `clearRect(x, y, width, height)`: 특정 캔버스 영역 지우기
* **스타일 설정 & 텍스트/이미지 렌더링**:
  * `strokeStyle`, `fillStyle`, `lineWidth`
  * `fillText("텍스트", x, y)`, `strokeText("텍스트", x, y)`
  * `drawImage(imageObj, x, y, width, height)`
* **인터랙티브 그래픽 애플리케이션**:
  * `mousedown`, `mousemove`, `mouseup` 마우스 이벤트를 캔버스 Coordinate와 연동하여 실시간 그래픽/그림판 앱 구현.

```javascript
// HTML5 Canvas 2D 그래픽 예시 코드
const canvas = document.getElementById("myCanvas");
const ctx = canvas.getContext("2d");

// 1. 파란색 사각형 그리기
ctx.beginPath();
ctx.rect(20, 20, 100, 60);
ctx.strokeStyle = "blue";
ctx.lineWidth = 2;
ctx.stroke();

// 2. 채워진 원 그리기
ctx.beginPath();
ctx.arc(180, 50, 30, 0, Math.PI * 2, false);
ctx.fillStyle = "violet";
ctx.fill();

// 3. 캔버스에 텍스트 렌더링
ctx.font = "bold 16px sans-serif";
ctx.fillStyle = "#222";
ctx.fillText("HTML5 Canvas API", 20, 120);
```

---

## 🛠️ Stack & Tools
- **Languages**: HTML5, CSS3, JavaScript (ES6+)
- **Graphics API**: HTML5 Canvas 2D Context API
- **Tools**: VS Code, Git / GitHub, Chrome DevTools
- **Standards**: W3C Web Standards & Responsive Design Compliance
