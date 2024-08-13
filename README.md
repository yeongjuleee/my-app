# my-app
현장에서 바로 써먹는 리액트 with 타입스크립트, 김정헌, 심통
* 2024/08/09 ~
---
## `Ctrl + C + 백틱 ` 으로 VS Code 터미널 열기 
Ctrl + C + ` 을 눌러 터미널을 실행한다. 

## create-react-app 으로 프로젝트 생성 및 실행
```
npx create-react-app <프로젝트명>
```

## 리액트 프로젝트 실행 
```
cd 프로젝트명 // 프로젝트 파일로 이동하는 명령어
npm start // 리액트 프로젝트 실행
```
---
## create-react-app 프로젝트 폴더 구조
크게 public 폴더와 src폴더를 확인할 수 있다. 
* `public` 폴더에는 리액트 프로젝트에 필요한 `HTML` 파일과 `favicon`등 정적(`Static`)파일들이 담겨있다.
* `src` 폴더에는 실제로 리액트를 가지고 프로그래밍을 할 자바스크립트(`Javascript`)파일을 보관하고 있다. 

리액트도 웹 서비스로 기본적으로 HTML 파일이 필요하다. `./public/index.html`이 해당 역할을 맡고 있으며, 우리가 만든 리액트 앱이 이 HTML 파일 위에 표시되게 된다. 

### 1. `./public/index.html` 
`<div id="root"></div>` : 사용자가 개발한 리액트 애플리케이션이 표시되는 부분 

### 2. `src/index.js.` 
```
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
        <React.StrictMode>
            <App />
        </React.StrictMode>
);
```
HTML의 div 태그에 리액트 애플리케이션을 삽입하는 코드이다. HTML의 요소(`Element`)를 `document.getElementById('root')`를 사용하여 찾는 것을 알 수 있다. 

`ReactDOM.createRoot`를 통해 리액트 프로젝트를 생성한 후 `render`함수를 통하여 root 요소에 <APP />를 표시하는 것을 알 수 있다.