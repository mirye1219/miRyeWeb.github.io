## WAI-ARIA?

> W3C의 WAI(Web Accessibility Initiative)가 제정한 RIA의 웹 접근성에 대한 표준 기술 규격.
>
> WAI는 Web Accessibility Initiative의 약자를 의미하고, ARIA는 Accessible Rich Internet Applications의 약자로서, 웹 콘텐츠와 웹 어플리케이션을 제작할 때 장애인을 위한 접근성 향상 방법을 정의.
>
> 특히, Ajax/HTML/Jaca Script 등의 기술로 개발된 동적인 콘텐츠, UI 컨트롤 개발할때 도움

### WAI-ARIA의 3대 요소

> 역할(role), 상태(state), 속성(property)을 통하여 유저인터페이스의 요소들을 정의하여 인식하기 쉽게 만듦.

#### 

#### 역할(role) - 랜드마크(이정표) 역할

> 1. 체크박스(checkbox), 버튼(button), 상태바(progress) 등을 포함하는 위젯 역할
> 2. 아티클(article), 이미지(img), 장식요소(presetntation)등 문서 구조역할
> 3. 메인영역(main), 검색영역(search), 네비게이션(navigation) 등 랜드마크(이정표)역할

```
어떤 요소가 메뉴 영역인지 콘텐츠 영역인지 푸터영역인지 등을 선언할 수 있다. 랜드마크 역할(role)을 지원하는 스크린리더는 시각장애인이 랜드마크로 지정한 주요 영역을 단축키 혹은 간단한 제스쳐로 왔다갔다 할 수 있게 해준다. 이는 스킵 네비게이션이 발전한 형태.

```

#### 상태(state) & 속성(property)

> 유저 인터페이스에 포함된 특정 컴포넌트의 속성과 상태 정보를 정의하며, 속성명에 'aria-'라는 접두사를 사용
>
> 1. 자동완성(aria-autocomplete), 체크여부(aria-checked)등을 포함하는 위젯 속성
> 2. 실시간 업데이트(aria-live)등을 포함하는 라이브 영역 속성
> 3. 드래그 앤 드롭 기능을 포함하는 드래그앤드롭 속성
> 4. DOM 요소들간의 관계를 정의하는 관계속성

### WAI-ARIA의 장점

> 1. 엘리먼트 및 컴포넌트에 누락된 의미를 제공할 수 있도록 한다.
> 2. 보조 기기 사용성을 향상 시킬 수 있다.
> 3. 논리적 구조 설계 가능 및 구조의 시각화가 가능하다.
> 4. 구조에 의미를 부여함으로 페이지 영역의 빠른 탐색이 가능하다.
> 5. 동적 컨텐츠의 식별이 가능하다.
> 6. 상태 변화 발생시 사용자 에이전트는 사용하는 API에 적절한 이벤트 알림을 제공한다.

## CSS 속성

### Inline 속성

> 줄을 바꾸지 않고 해당 위치에서 필요로 하는 폭만 유지해 다른 요소들과 같은 라인에 위치하려는 성질
>
> **Inline성질을 갖는 요소**
>
> `span, a, strong, em, img, input…`
>
> **특징**
>
> - 상, 하단 margin 속석이 적용되지 않는다.
> - 너비(width)와 높이(height)속성이 적용되지 않는다.
> - Inline 속성을 가진 태그끼리 연속해서 사용되는 경우, 변도의 속성이 정의되어 있지 않으면 좌, 우에 약 5px가량의 margin속성이 적용된다

### Block 속성

> 새로운 줄에서 시작되며 전체 좌우 너비 (width)를 100% 사용하는 요소들
>
> **Block 성질을 갖는 요소**
>
> `html, address, blockquote, body, div, dl, dt, fieldset, form, frame, h1~6, ol, p, ul, center, dir, hr, footer, canvas…`
>
> **주의할 점**
>
> - Block 성질을 갖는 요소는 Inline 성질을 갖는 요소보다 상위요소
>
> ​ => Inline 성질을 갖는 요소 내부에 Block 성질을 갖는 요소를 포함할 수는 없음.

### Inline-Block

> 기본적으로 Inline 성질을 갖지만 Block처럼 margin, width, height 등의 속성을 정의하면 이를 표현
>
> -CSS를 통해 따로 선언
>
> `display:inline-block`