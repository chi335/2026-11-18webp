# 🌐 Web Programming & Front-End Core Study Notes

> 웹 개발 입문 및 환경 구축(바이브 코딩 등)부터 **HTML5 시맨틱 구조 설계, CSS3 스타일 규칙 및 레이아웃, JavaScript와 브라우저 엔진 동작 원리, HTML5 Canvas 2D 그래픽스 프로그래밍**

---

## 📌 목차 (Table of Contents)
1. [01. 바이브 코딩 입문과 환경 준비](#1-01-바이브-코딩-입문과-환경-준비)
2. [02. HTML 구조와 정보 설계](#2-02-html-구조와-정보-설계)
3. [03. CSS 기본과 스타일 규칙 및 예제](#3-03-css-기본과-스타일-규칙-및-예제)
4. [04. JavaScript와 브라우저의 역할](#4-04-javascript와-브라우저의-역할)
5. [11. HTML5 캔버스 그래픽 (Canvas API)](#5-11-html5-캔버스-그래픽-canvas-api)

---

## 1. 01. 바이브 코딩 입문과 환경 준비

웹 생태계의 패러다임과 현대적인 웹 개발 트렌드(AI/바이브 코딩), 개발 환경 구축 및 웹 표준 개념을 정리합니다.

### 💡 핵심 정리
* **바이브 코딩 (Vibe Coding)**:
  * 생성형 AI 어시스턴트(Copilot, ChatGPT 등)를 활용하여 빠른 프로토타이핑과 개발 생산성을 극대화하는 코딩 방식.
  * 기초 웹 기술(HTML/CSS/JS)의 원리를 명확히 이해해야 AI가 생성한 코드를 검증하고 리팩토링 가능.
* **웹 개발 3대 요소의 역할 구분**:
  * **HTML (HyperText Markup Language)**: 웹 문서의 데이터 및 뼈대 구조 정의
  * **CSS (Cascading Style Sheets)**: 비주얼 스타일링, 레이아웃 및 디자인 표현
  * **JavaScript**: 웹 문서의 동적 제어, 비동기 통신(AJAX/Fetch) 및 사용자 인터랙션
* **개발 환경 구축 (Development Environment)**:
  * **Code Editor**: Visual Studio Code (VS Code)
  * **Essential Extensions**: Live Server (로컬 개발 서버), Prettier (코드 포맷팅), ESLint (문법 검사)
  * **Debugging Tool**: Chrome DevTools (Elements, Console, Network, Application 탭 활용)
* **웹 표준(Web Standards) & 웹 접근성(A11y)**:
  * W3C 규격 준수 ➔ 크로스 브라우징(Cross-Browsing) 보장
  * 반응형 웹 디바이스 대응 (`<meta name="viewport" content="width=device-width, initial-scale=1.0">`)

---

## 2. 02. HTML 구조와 정보 설계

웹 문서의 정보 구조화(Information Architecture)와 시맨틱 태그를 활용한 웹 접근성/SEO 최적화를 다룹니다.

### 💡 핵심 정리
* **HTML5 표준 문서 구조**:
  * `<!DOCTYPE html>` 선언 및 `<html>`, `<head>`, `<body>` 태그 기반 구획 정의.
* **시맨틱 태그 (Semantic Tags)**:
  * 단순 구획 분리가 아닌 **의미(Meaning)**를 부여하여 검색 엔진(SEO) 및 스크린 리더 접근성 향상.
  * `<header>`: 상단 헤더 (로고, 메인 메뉴 등)
  * `<nav>`: 네비게이션 메뉴 바
  * `<main>`: 해당 문서의 핵심 유일 콘텐츠
  * `<section>`: 주제별 논리적 단락 구획
  * `<article>`: 독립적으로 분리 가능한 콘텐츠 (포스트, 뉴스 기사 등)
  * `<aside>`: 사이드바 및 부가 정보
  * `<footer>`: 하단 저작권, 연락처 정보
* **폼(Form) 및 데이터 전송 구조**:
  * 사용자 입력을 백엔드로 전송하기 위한 통로 (`<form action="..." method="POST">`)
  * `<input type="text|email|password|checkbox|radio">`, `<select>`, `<textarea>`, `<button>`
  * 속성: `name`, `value`, `placeholder`, `required`, `pattern` (유효성 검사)

---

## 3. 03. CSS 기본과 스타일 규칙 및 예제

웹 디자인 표현력 강화를 위한 CSS 규칙, 박스 모델, 레이아웃 기법(Flexbox, Grid, Position)을 정리합니다.

### 💡 핵심 정리
* **CSS 적용 3가지 방식**:
  1. Inline (`style="..."`) - 유지보수에 비효율적
  2. Internal (`<style>` 태그)
  3. External (`<link rel="stylesheet" href="style.css">`) - 모듈화 및 캐싱 최적화
* **선택자 (Selectors) 및 우선순위 (Specificity)**:
  * `*` (전체) < `태그` < `.클래스` < `#ID` < Inline Style < `!important`
  * 가상 클래스/요소: `:hover`, `:focus`, `:nth-child(n)`, `::before`, `::after`
* **박스 모델 (Box Model)**:
  * `Margin` ➔ `Border` ➔ `Padding` ➔ `Content`
  * 박스 크기 계산 오차 방지를 위해 `box-sizing: border-box;` 필수 적용.
* **레이아웃(Layout) 핵심 시스템**:
  * **Flexbox (1D Layout)**: `display: flex`, `flex-direction`, `justify-content` (주축 정렬), `align-items` (교차축 정렬)
  * **Grid (2D Layout)**: `display: grid`, `grid-template-columns`, `gap`
  * **Positioning**: `static`, `relative`, `absolute`, `fixed`, `sticky`

---

## 4. 04. JavaScript와 브라우저의 역할

자바스크립트 언어 기본과 브라우저 엔진의 렌더링 파이프라인, DOM/BOM 제어 구조를 살펴봅니다.

### 💡 핵심 정리
* **브라우저 렌더링 파이프라인 (Critical Rendering Path)**:
  1. **HTML/CSS Parsing** ➔ DOM Tree & CSSOM Tree 생성
  2. **Render Tree 구축** ➔ 화면에 보일 노드만 결합
  3. **Layout (Reflow)** ➔ 각 노드의 정확한 위치/크기(픽셀) 계산
  4. **Paint (Repaint)** ➔ 화면의 픽셀 단위로 색상 및 이미지 드로잉
* **DOM (Document Object Model) 제어**:
  * HTML 요소를 객체(Object)로 추상화하여 자바스크립트로 조작.
  * `document.querySelector()`, `document.querySelectorAll()`
  * `element.textContent`, `element.classList.add()`, `element.appendChild()`
* **이벤트 처리 및 이벤트 흐름**:
  * **이벤트 전달 3단계**: Capturing ➔ Target ➔ Bubbling
  * **이벤트 위임 (Event Delegation)**: 부모 요소에 단일 이벤트를 등록하여 동적 자식 요소의 이벤트를 효율적으로 처리.

---

## 5. 11. HTML5 캔버스 그래픽 (Canvas API)

플러그인(Flash 등) 없이 자바스크립트를 사용하여 브라우저 상에 2D 그래픽, 애니메이션, 대화형 게임 및 실시간 차트를 직접 렌더링하는 기술입니다.

### 💡 핵심 정리
* **HTML5 Canvas 도입 배경**:
  * 기존 플러그인(Flash, Java Applet 등) 방식에서 벗어나 표준 브라우저 및 모바일 단말에서 자바스크립트 기반 그래픽 출력을 지원하는 `<canvas>` 태그 도입.
  * 웹이 문서를 보여주는 수준을 넘어 응용 프로그램으로 진화하는 핵심 기반 제공.
* **`<canvas>` 태그 및 렌더링 컨텍스트 (Context)**:
  * 웹 페이지 내 Graphic 영역을 할당 (`width`, `height` 디폴트: 300x150 픽셀).
  * `canvas.getContext("2d")` 메서드로 2D 그래픽을 그리는 컨텍스트(도구) 획득.
* **경로(Path) 기반 도형 그리기**:
  * `beginPath()`: 새로운 빈 경로(Path) 시작
  * `moveTo(x, y)`: 펜의 시작 위치 이동
  * `lineTo(x, y)`: 직선 경로 추가
  * `rect(x, y, w, h)`: 경로에 사각형 삽입
  * `strokeRect(x, y, w, h)` / `fillRect(x, y, w, h)`: 직접 사각형 렌더링
  * `arc(x, y, r, startAngle, endAngle, anticlockwise)`: 원호 및 원 경로 생성
  * `stroke()`: 생성된 경로를 따라 외곽선 렌더링
  * `fill()`: 경로 내부를 설정된 색상으로 채우기
  * `clearRect(x, y, w, h)`: 지정 영역 지우기
* **스타일 설정, 텍스트 및 이미지 출력**:
  * `strokeStyle`, `fillStyle`, `lineWidth`: 선 색상, 채우기 색상 및 선 굵기 프로퍼티
  * `fillText("텍스트", x, y)`, `strokeText("텍스트", x, y)`: 텍스트 출력
  * `drawImage(imgObj, x, y, width, height)`: 이미지 객체 렌더링
* **인터랙티브 그래픽 애플리케이션**:
  * `mousedown`, `mousemove`, `mouseup` 이벤트를 조합하여 마우스 궤적 좌표를 계산해 실시간 그림판/드로잉 앱 구현.

---

## 🛠️ Tech Stack & Environment
- **Languages**: HTML5, CSS3, JavaScript (ES6+)
- **Graphics API**: HTML5 Canvas 2D Context API
- **Tools**: Visual Studio Code, Git / GitHub, Chrome DevTools
- **Target Standard**: W3C Web Standards & Responsive Web Design Compliance
