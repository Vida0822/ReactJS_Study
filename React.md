## React 설치 



#### 1. 두개의 javascript 코드 import

https://reactjs.org/docs/add-react-to-a-website.html#tip-minify-javascript-for-production
- https://unpkg.com/react@18/umd/react.production.min.js
- https://unpkg.com/react-dom@18/umd/react-dom.production.min.js

<!DOCTYPE html>
<html>
  <body></body>
  <script src="https://unpkg.com/react@18/umd/react.production.min.js"></script>
  <script src="https://unpkg.com/react-dom@18/umd/react-dom.production.min.js"></script>
</html>

```html
<!DOCTYPE html>
<html>
  <body></body>
  <script src="https://unpkg.com/react@18/umd/react.production.min.js"></script>
  <script src="https://unpkg.com/react-dom@18/umd/react-dom.production.min.js"></script>
</html>

```



#### 2. Console 확인

정적 페이지 로드 --> console에 'React'

```ba
Rea
Uncaught ReferenceError ReferenceError: Rea is not defined
    at <anonymous> (repl:1:1)
React
{Children: {…}, Component: ƒ, Fragment: Symbol(react.fragment), Profiler: Symbol(react.profiler), PureComponent: ƒ, …}
__SECRET_INTERNALS_DO_NOT_USE_OR_YOU_WILL_BE_FIRED: {ReactCurrentDispatcher: {…}, ReactCurrentOwner: {…}, ReactCurrentBatchConfig: {…}, Scheduler: {…}}
Children: {map: ƒ, forEach: ƒ, count: ƒ, toArray: ƒ, only: ƒ}
cloneElement: ƒ (a,b,c){if(null===a||void 0===a)throw Error("React.cloneElement(...): The argument must be a React element, but you passed "+\na+".");var e=ka({},a.props),d=a.key,k=a.ref,h=a._owner;if(null!=b){void 0!==b.ref&&(k=b.ref,h=L.current);void 0!==b.key&&(d=""+b.key);if(a.type&&a.type.defaultProps)var l=a.type.defaultProps;for(f in b)aa.call(b,f)&&!ba.hasOwnProperty(f)&&(e[f]=void 0===b[f]&&void 0!==l?l[f]:b[f])}var f=arguments.length-2;if(1===f)e.children=c;else if(1<f){l=Array(f);for(var g=0;g<f;g++)l[g]=arguments[g+2];e.children=l}return{$$typeof:y,type:a.type,key:d,ref:k,props:e,_owner:h}}
Component: ƒ w(a,b,e){this.props=a;this.context=b;this.refs=W;this.updater=e||X}
createContext: ƒ (a){a={$$typeof:va,\n_currentValue:a,_currentValue2:a,_threadCount:0,Provider:null,Consumer:null,_defaultValue:null,_globalName:null};a.Provider={$$typeof:ua,_context:a};return a.Consumer=a}
createElement: ƒ Z(a,b,\ne){var m,d={},c=null,h=null;if(null!=b)for(m in void 0!==b.ref&&(h=b.ref),void 0!==b.key&&(c=""+b.key),b)aa.call(b,m)&&!ba.hasOwnProperty(m)&&(d[m]=b[m]);var l=arguments.length-2;if(1===l)d.children=e;else if(1<l){for(var f=Array(l),k=0;k<l;k++)f[k]=arguments[k+2];d.children=f}if(a&&a.defaultProps)for(m in l=a.defaultProps,l)void 0===d[m]&&(d[m]=l[m]);return{$$typeof:y,type:a,key:c,ref:h,props:d,_owner:L.current}}
createFactory: ƒ (a){var b=Z.bind(null,a);b.type=a;return b}
createRef: ƒ (){return{current:null}}
forwardRef: ƒ (a){return{$$typeof:wa,render:a}}
Fragment: Symbol(react.fragment)
isValidElement: ƒ M(a){return"object"===typeof a&&null!==a&&a.$$typeof===y}
lazy: ƒ (a){return{$$typeof:za,_payload:{_status:-1,_result:a},_init:qa}}
memo: ƒ (a,b){return{$$typeof:ya,type:a,\ncompare:void 0===b?null:b}}
Profiler: Symbol(react.profiler)
PureComponent: ƒ K(a,b,e){this.props=a;this.context=b;this.refs=W;this.updater=e||X}
startTransition: ƒ (a,b){b=J.transition;J.transition={};try{a()}finally{J.transition=b}}
StrictMode: Symbol(react.strict_mode)
Suspense: Symbol(react.suspense)
unstable_act: ƒ (a){throw Error("act(...) is not supported in production builds of React.");}
useCallback: ƒ (a,b){return g.current.useCallback(a,b)}
useContext: ƒ (a){return g.current.useContext(a)}
useDebugValue: ƒ (a,b){}
useDeferredValue: ƒ (a){return g.current.useDeferredValue(a)}
useEffect: ƒ (a,b){return g.current.useEffect(a,\nb)}
useId: ƒ (){return g.current.useId()}
useImperativeHandle: ƒ (a,b,c){return g.current.useImperativeHandle(a,b,c)}
useInsertionEffect: ƒ (a,b){return g.current.useInsertionEffect(a,b)}
useLayoutEffect: ƒ (a,b){return g.current.useLayoutEffect(a,b)}
useMemo: ƒ (a,b){return g.current.useMemo(a,b)}
useReducer: ƒ (a,b,c){return g.current.useReducer(a,b,c)}
useRef: ƒ (a){return g.current.useRef(a)}
useState: ƒ (a){return g.current.useState(a)}
useSyncExternalStore: ƒ (a,b,c){return g.current.useSyncExternalStore(a,b,c)}
useTransition: ƒ (){return g.current.useTransition()}
version: '18.2.0'
[[Prototype]]: Object

```





## 2. THE BASICS OF REACT ()

###  

### 1. React 사용 이유 : By createElement (어려운 방식)

#### 1. React JS 가 Element 를 다루는 방식 때문! 

*  react-dom : React element 를 html에 두는 역할

  (vs React js : 어플리케이션이 interactive하도록 만들어주는 library !)

=> html 을 페이지에 직접 작성하지 않음

=> java script를 활용해 element 생성

```html
<!DOCTYPE html>
<html>
  <body>
    <div id="root"></div>
  </body>

  <!--하드 코딩으로 React 적용되게 만듬 -> 나중엔 이런 모든 것이 포함된 React JS 프로젝트 만드는법 배움 ! -->
  <script src="https://unpkg.com/react@18/umd/react.production.min.js"></script>
  <script src="https://unpkg.com/react-dom@18/umd/react-dom.production.min.js"></script>

  <script>
     //어려운 방법 (사용 x) -> but 이해해야 rect 본질 이해 가능 
    const root = document.getElementById("root"); 
    const span = React.createElement(
      "span",
      { id: "sexy-span", style: { color: "red" } }, // 두번째 argument : span의 property
      "Hello I'm span" //  세번째 argument : content
    );
    ReactDOM.createRoot(root).render(span); // render : show to user (what, where)

  </script>
</html>

```



=> body html에 div 빼고 아무것도 작성해주지 않았지만 실제로 속성까지 다 갖춘 span태그 생성 됨 



##### React의 동작 원리 ** 

* 기존 바닐라 js : html로 --> javascript --> html 

  ​			; html을 만들고, 찾아서 가져오고, 그걸 가져와 작업(편집)해 다시 html로 update

* React js : js ---> html 

  ​		; react가 여러가지 작업을 처리 한후 html 결과물을 업데이트) 

  ​		=> html 코드를 작성할 필요 없음 (user한테 보여줄 내용 control 가능)



##### 주요 함수 

```javascript
// 1.  createElement (요소명, property or event , content ) : 여러 설정작업과 함께 요소 생성 
React.createElement(
      "span",
      { id: "sexy-span", style: { color: "red" } },
      "Hello I'm span"
    );

// 2. createRoot() : dom 을 작성할 root를 지정 
const root = ReactDOM.createRoot(root)

// 3. render() : 사용자(화면)에 보여줌 <-> html에 실제로 작성함
root.render(span); 
```





+) error

```javascript
React.createElement("root") //  --> Minified React error #299 ("root" 라는 이름의 html 태그는 없으니 찾질 못함)
```





#### 2. 이벤트 Listen 

프론트 개발자 목적 : interactive web page , 즉 eventListen에 따른 반응처리가 목적임을 암

=> 이걸 React는 알고 있음 ! -->  event를 훨씬 편한 방식으로 등록하도록 해줌 !!

=> // java script로 요소를 만들고 html로 바꾸는 방식의 장점



#### Vanila js VS React js - 버튼 만들기

##### Vanila js

````html
<!DOCTYPE html>
<html>
  <body>
    <span>Total clicks : 0 </span>
    <button id="btn">Click me</button>

    <script>
      var counter = 0; // 이거 0 안해주면 NaN(var은 괜찮)

      const button = document.getElementById("btn");
      const span = document.querySelector("span");

      function handleClick() {
        counter = counter + 1; 
        span.innerText = `Total clicks : ${counter}`;
      }
      button.addEventListener("click", handleClick);
    </script>
  </body>
</html>

````

html 문서에 span 태그 작성

 --> html 문서에 button 태그 작성

 --> get ElementByID로 span태그 가져오기

 --> get ElementByID로 button태그 가져오기

--> 핸들러 함수 생성 

--> addEventLister로 버튼에 event 걸어주기 

--> 다시 html 에 반영 



**vs** 

##### React js

```html
<!DOCTYPE html>
<html>
  <body>
    <div id="root"></div>
  </body>

  <script src="https://unpkg.com/react@18/umd/react.production.min.js"></script>
  <script src="https://unpkg.com/react-dom@18/umd/react-dom.production.min.js"></script>

  <script>
    const root = document.getElementById("root");
    const h3 = React.createElement(
      "h3",
      {
        onMouseEnter: () => console.log("mouse enter"),
      },
      "Hello I'm span"
    );

    const btn = React.createElement(
      "button",
      {
        // property에 eventListener 속성 줌!
        onClick: () => console.log("i'm clicked"),
        // but 얘는 실제 html 태그에 표시되진 않음 (얘는 html에 표시할 필요가 없는 정보임을 react 는 암) , 반면 id 속성을 두면 web tag 에 표시됨 : 이 preperty는 html에 놓여야하는것을 암 (알아서 문서 구성잘해줌! )
        // <-> on 어쩌구는 두지 않음
        style: {
          backgroundColor: "tomato",
        },
      },
      "Click me"
    );
    // React로 but on 요소를 만드니 한 문장안에 content도 넣고, property도 지정하고 심지어 eventListener까지 지정 가능 !


    const container = React.createElement("div", null, [h3, btn]);
    // content으로 두개 태그 넣어줌 (배열 형태) - 두개의 component를 가진 component를 생성해줌 !
    ReactDOM.createRoot(root).render(container);
  </script>
</html>

```

h3 태그 생성 (+ 이벤트 걸어줌, content 작성함 )

--> button 태그 생성 (+ 이벤트 걸어줌, 스타일 속성줌 ,content 작성함)

--> html 태그에 작성해줌 



* react JS --> interactive power (element 생성, add event Listener )8 

* React Dom --> Element를 가져다 html 로 바꿔줌 





### 2. createElement 대체 : jsx (대부분 사용)

* 더 comportable tool : jsx (js 확장 문법)

* 생긴게 html과 비슷해 더 편리 (우린 앞에서 jsx의 내부동작을 본거임)

==> 우리는 인간 친화적인 jsx 코드로 소스코드를 작성하고, 변환기가 그걸  브라우저가 이해할 수 있는 코드로 바꿔서 전달 

​	(**jsx --> Bebel --> 브라우저**)



#### 1. 변환기 설치 : Babel standalone

​	 = jsx 코드를 : jsx 로 적은 코드가createElement 형식으로 내부적으로 바꿔서 브라우저에 전달) 

​      --> createElement 로 바꿔서 브라우저에 전달

* 브라우저가 JSX를 이해할 수 있게 뭔가를 설치 

```html
<script src="https://unpkg.com/@babel/standalone/babel.min.js"></script> <!--1-->

<script type="text/babel"> // 2 
	// 스크립트 코드   
</script> 
```



#### 2. jsx 로 Element 만들기 

```react

  <script src="https://unpkg.com/react@18/umd/react.production.min.js"></script>
  <script src="https://unpkg.com/react-dom@18/umd/react-dom.production.min.js"></script>
  <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>

  <script type="text/babel">
    const root = document.getElementById("root");
    const title = (
      <h3 id="title" onMouseEnter={() => console.log("MouseEnter")}>
        "Hello I'm title"
      </h3>
    ); // 진짜 html 문법으로 적어주면 됨! (그전 바닐라 js에는 문자를 만들어 올려주는 기능 )

    const btn = (
      <button
        style={{
          backgroundColor: "tomato",
        }}
        onClick={() => console.log("im clicked")}
      >
        Click me
      </button>
    );

    const Container = React.createElement("div", null, [title, btn]);
    ReactDOM.createRoot(root).render(container);
  </script>

```



=> 브라우저에 전달 된 코드 : 우리가 앞에서 배운 코드로 변환 

```html
<head><script>
"use strict";

var root = document.getElementById("root");
var title = /*#__PURE__*/React.createElement("h3", {
  id: "title",
  onMouseEnter: function onMouseEnter() {
    return console.log("MouseEnter");
  }
}, "\"Hello I'm title\""); // 진짜 html 문법으로 적어주면 됨! (그전 바닐라 js에는 문자를 만들어 올려주는 기능 )

var btn = /*#__PURE__*/React.createElement("button", {
  style: {
    backgroundColor: "tomato"
  },
  onClick: function onClick() {
    return console.log("im clicked");
  }
}, "Click me");
var container = React.createElement("div", null, [title, btn]);
</script></head>
```





#### 3. jsx로 컴포넌트 in another 컴포넌트 

** **중요 : 직접 만든 컴포넌트를 다른 곳에서 사용할 때는 반!드!시! 대문자로 (아님 일반 html 요소와 헷갈림) ** 

=> jsx는 어플리케이션을 여러가지 작은 요소로 나누어 관리할 수 있게 해준다 ! 

 (seperate  : 코드(요소 생성)를 분리 한 후 함께 랜더링 ) 



```react
<!DOCTYPE html>
<html>
  <body>
    <div id="root"></div>
  </body>

  <!--하드 코딩으로 React 적용되게 만듬 -> 나중엔 이런 모든 것이 포함된 React JS 프로젝트 만드는법 배움 ! -->
  <script src="https://unpkg.com/react@18/umd/react.production.min.js"></script>
  <script src="https://unpkg.com/react-dom@18/umd/react-dom.production.min.js"></script>
  <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>

  <script type="text/babel">
    const root = document.getElementById("root");
    function Title() {
      return (
        <h3 id="title" onMouseEnter={() => console.log("MouseEnter")}>
          "Hello I'm title"
        </h3>
      );
    }

    const Button = () => (
      <button
        style={{
          backgroundColor: "tomato",
        }}
        onClick={() => console.log("im clicked")}
      >
        Click me
      </button>
    );

    // 만들어진 react로 태그들을 다른 태그에 포함하는 과정
    //  const Container = <div>title Button</div>;
    const Container = () => (
      // 위에 정의해준 Title 을 가져와 넣어주는 jsx의 문법
      // 대문자여야야함 : 아니면 그냥 일반 html 태그 종류 (html 버튼 ) 이라고 생각
      // 여기에서 작성해준 button임을 알릴려면 무조건 uppercase로 앞글자 맞춰줘야함
      <div>
        <Title />
        <Button />
      </div>
    );
    ReactDOM.createRoot(root).render(<Container />);
  </script>
</html>

```



=> 브라우저에 전달된 코드 (create Element 투성이 --> jsx 없었으면 이렇게 작성해야함 )

```html
<head><script>"use strict";

var root = document.getElementById("root");
function Title() {
  return /*#__PURE__*/React.createElement("h3", {
    id: "title",
    onMouseEnter: function onMouseEnter() {
      return console.log("MouseEnter");
    }
  }, "\"Hello I'm title\"");
}
var Button = function Button() {
  return /*#__PURE__*/React.createElement("button", {
    style: {
      backgroundColor: "tomato"
    },
    onClick: function onClick() {
      return console.log("im clicked");
    }
  }, "Click me");
};

// 만들어진 react로 태그들을 다른 태그에 포함하는 과정
//  const Container = <div>title Button</div>;
var Container = function Container() {
  return (
    /*#__PURE__*/
    // 위에 정의해준 Title 을 가져와 넣어주는 jsx의 문법
    // 대문자여야야함 : 아니면 그냥 일반 html 태그 종류 (html 버튼 ) 이라고 생각
    // 여기에서 작성해준 button임을 알릴려면 무조건 uppercase로 앞글자 맞춰줘야함
    React.createElement("div", null, /*#__PURE__*/React.createElement(Title, null), /*#__PURE__*/React.createElement(Button, null))
  );
};
ReactDOM.createRoot(root).render( /*#__PURE__*/React.createElement(Container, null));
</script>
</head>
```

