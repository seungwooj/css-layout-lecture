### 3. SCSS

#### 3.0 What is SCSS? (<a href="https://sass-lang.com/guide">Link</a>)

- **SCSS : CSS Preprocessor → compile SCSS and make normal CSS**
- SCSS makes CSS like a programming language! (variables, functions...)  
  (**npm / gulp를 사용해서 scss의 내용이 자동으로 css로 compile되게끔 구성되어 있음**)
  (gulp? (<a href="https://ko.wikipedia.org/wiki/Gulp.js">Link</a>) - npm기반 빌드 시스템. 테스트시 에러 등 확인 가능.)
- 환경설정
  1. npm install → npm run dev 실행: gulpfile의 내용을 활용하여 빌드 시스템을 실행
  2. gulpfile속의 scss, css의 경로를 확인
  3. HTML에 css의 경로가 셋팅되어 있는지 확인 (browser doesnot understand scss!)

#### 3.1 Variables and Nesting

- Grid : flexbox로 Grid(표)를 만들기가 어려워서 Grid전용 컨셉이 등장한 것
