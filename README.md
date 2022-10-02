# NodeJS_Basic

## Chapter1 : Start

> NodeJS는 VanillaJS와 어떻게 다를까?

1.  Node runs on a server - not in a browser
2.  The console is the terminal window
3.  Global object instead of window object
4.  Has common core modules
5.  CommonJS modules instead of ES6 modules
6.  Missing some JS apis like fetch api

## Chapter2 : Read and Write Files

> File 모듈을 이용한 파일 읽기/쓰기/수정

1. fs.readFile : 파일 읽기
2. fs.writeFile : 파일 쓰기
3. fs.appendFile : 파일 쓰기 + 추가
4. fs.rename : 파일명 변경

> 비동기코드의 동기화

1. using callback
2. using async-await with fsPromises

> 용량이 큰 파일을 읽거나 수정할때, to grab bucket by bucket is better than to grab all at once

1. fs.createReadStream
2. fs.createWriteStream

> 디렉토리 생성/삭제

1. fs.existsSync : 디렉토리 존재여부 확인
2. fs.mkdir : 디렉토리 생성
3. fs.rmdir : 디렉토리 삭제

## Chapter3 : NPM Modules

> NPM Module와 Node common core modules

1. NPM : node modules that are created by third parties (by other developers)
2. npm i nodemon -g :
   1. install a package _globally_
   2. nodemon monitors and automatically restarts server when changes occur
3. npm init : initialize npm just for _my project_ -> generates package.json file

> package.json

1. 특정 프로젝트에서 사용하고있는 npm 패키지들을 명세하고있는 파일
2. npm패키지를 다운받으면 용량이 큰 node_modules 폴더가 생기는데 이를 github에 그대로 올리지 않고(.gitignore 파일을 이용), 해당 패키지명을 명시한 package.json만을 이용하여 npm install 명령어로 유관 패키지 모듈들을 다운로드받아 프로젝트를 셋업할 수 있음.
