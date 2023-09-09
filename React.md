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
