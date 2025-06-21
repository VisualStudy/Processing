# Processing
Processing 강의 소스 모음

## 1단계: Processing의 최소 구조 익히기

### 기본 구조

```java
void setup() {
  size(600, 400); // 화면 크기
}

void draw() {
  background(255);       // 배경색 흰색으로 초기화
  ellipse(300, 200, 100, 100);  // 화면 중앙에 원
}
```

#### 설명:

* `setup()`은 **딱 한 번** 실행되는 초기 설정 함수이다.
* `draw()`는 매 프레임(기본 60fps)마다 반복 실행되는 함수이다.
* `ellipse(x, y, w, h)`는 타원(원이 될 수도)을 그린다.

---

## 2단계: 마우스를 따라다니는 원

```java
void setup() {
  size(600, 400);
  background(255);
}

void draw() {
  background(255); // 매 프레임마다 배경 초기화
  ellipse(mouseX, mouseY, 50, 50); // 마우스 위치에 원
}
```

#### 핵심 개념:

* `mouseX`, `mouseY`는 마우스 좌표를 자동으로 추적해주는 내장 변수.

---

## 3단계: 마우스 클릭 시 색이 바뀌는 원

```java
void setup() {
  size(600, 400);
  background(255);
}

void draw() {
  if (mousePressed) {
    fill(255, 0, 0);  // 빨간색
  } else {
    fill(0, 0, 255);  // 파란색
  }
  ellipse(mouseX, mouseY, 50, 50);
}
```

#### 핵심 개념:

* `mousePressed`: 마우스가 눌렸는지 여부 (`boolean`)
* `fill(r, g, b)`: 색상 지정 (RGB)

