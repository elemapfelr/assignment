# 왜 스벨트를 사용했나?

## 쉬운 학습 곡선

스벨트에는 어떠한 boilerplate(세팅용 상용구 코드)도 없고 문법이 HTML과 동일하여 기본 HTML, CSS, JS를 배운 사람이면 svelte를 사용할 수 있다.
사실 JS의 개발을 편하게 하기 위해 나온 도구가 프레임워크인데, 프레임워크의 학습곡선이 가파르면 오히려 진입장벽이 높아진다고 생각한다.

## No Virtual DOM

Svelte는 기존의 주류 프론트 프레임워크들 처럼 Run-time 환경에서 돌아가는게 아닌, 컴파일 단계에서 JS를 빌드하기 때문에 번들의 크기가 작고, 퍼포먼스 또한 뛰어나다.

## CSS 관리 용이

컴포넌트 단위로 CSS를 적용할 수 있어서 다른 컴포넌트에 영향을 주지 않아 이로 인해 스타일 충돌을 방지할 수 있다. [:global] 수식어를 사용하면 전역 스타일 적용 또한 가능하다.
PostCSS, SCSS와 같은 CSS Preprocessor(CSS 전처리기) 를 지원하기 때문에, 스타일 시트 작성이 용이하다.

# 왜 tailwindCSS를 사용했나?

## Utility-First의 편리함

HTML class 만으로 스타일을 적용할 수 있기에, 별도의 스타일 코드가 필요없다.
또한 태그의 클래스명을 고민할 필요가 없다.

## 일관된 스타일 적용

다양한 색상, 간격, 사이즈 등의 유틸리티 클래스가 정해져 있기에, 모든 컴포넌트에서 일관된 스타일로 디자인이 가능하다.

## Bootstrap 보다 로우 레벨의 스타일 적용 가능

CSS 요소 수준의 유틸리티 클래스를 제공하기 때문에 섬세하게 디자인 구현이 가능하다.
또한 config 파일의 extends 값을 수정하여 간편하게 커스텀이 가능하다.

## Styled Components (CSS in JS) 지양

JS로 CSS를 작성하는 방식은 기존에 브라우저의 렌더링이 StyleSheet와 Script로 나누어 병렬처리 하던 것을 Script 하나만으로 직렬처리 하기에 런타임 오버헤드가 발생할 수 있다.
또한 추가적인 JS 계산이 필요하기 때문에 성능에 영향을 준다.