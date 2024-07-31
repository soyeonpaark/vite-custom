# Vite 커스텀 템플릿

React 개발을 위한 나만의 vite 커스텀 템플릿 작성하기

---

1. 개발용 Vite 설치

   ```
   pnpm add vite -D # --save-dev
   ```

   </br>

2. 엔트리 파일 (index.html) 생성
   최소한의 접근성을 고려한 `<noscript>` 추가:

   ```html
   <noscript>
     <p>이 앱은 Javascript 활성화가 필요합니다.</p>
   </noscript>
   ```

    </br>

3. React 라이브러리 설치 (react, react-dom)

   ```
   pnpm add react react-dom
   ```

   </br>

4. favicon 최적화 및 등록
   </br>

5. 환경변수 `%MODE%` 사용
   </br>

6. React 및 Node 타입 선언 패키지 설치

   ```
   pnpm add @types/{react,react-dom,node} -D
   ```

   </br>

7. Vite 플러그인 (JSX runtime automatic)

   ```
   pnpm add @vitejs/plugin-react -D
   ```

   </br>

8. ESlint

- ESlint 초기 설정

  ```
  pnpm create @eslint/config@latest
  ```

- ESlint 실행 (src 디렉토리 파일 검사 / 비활성화 지시문 보고 / .gitignore 패턴 무시)

  ```
  pnpm eslint ./src --report-unused-disable-directives --ignore-pattern .gitignore
  ```

- React Hooks, React Refresh 추가 플러그인
  ```
  pnpm add eslint-plugin-react-hooks eslint-plugin-react-refresh -D
  ```
  </br>

9. 절대경로 설정 (jsconfig.json)
   ```json
   {
     "compilerOptions": {
       "baseUrl": ".",
       "paths": {
         "@/*": ["src/*"]
       }
     }
   }
   ```
   </br>

**.gitignore 설정**

```
.DS_Store
node_modules
build
dist
```
