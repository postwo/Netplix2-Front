# 설치 명령어
npx create-react-app [생성할 이름]

# 실행 명령어
npm run start

# 라우터 설치
npm install react-router-dom

# git bash 파일경롱 이동
cd 이동경로

# powershell
cd .\이동경로

# 백엔드는 8080 프론트는 3000이어서 프록시 해주는 기능을 설정 
package.json에다가  "proxy":"http://localhost:8080", 이거를 추가해주면 프록시 설정이 완료된거다.


# 카카오 로그인 에러 뜨는 이유
KakaoAuthRedirect.js:24  카카오 로그인 실패: TypeError: Cannot read properties of null (reading 'accessToken')
# 해결방안 
메인 index.js에서  <React.StrictMode> 이부분을 지운다.

npm error code ERESOLVE
npm error ERESOLVE unable to resolve dependency tree
npm error
npm error While resolving: netplix-front@0.1.0
npm error Found: react@19.0.0
npm error node_modules/react
npm error   react@"^19.0.0" from the root project
npm error
npm error Could not resolve dependency:
npm error peer react@"^18.0.0" from @testing-library/react@13.4.0
npm error node_modules/@testing-library/react
npm error   @testing-library/react@"^13.0.0" from the root project
npm error
npm error Fix the upstream dependency conflict, or retry
npm error this command with --force or --legacy-peer-deps
npm error to accept an incorrect (and potentially broken) dependency resolution.npm error
npm error
npm error For a full report see:
npm error C:\Users\codo7\AppData\Local\npm-cache\_logs\2024-12-06T08_37_41_023Z-eresolve-report.txt
npm error A complete log of this run can be found in: C:\Users\codo7\AppData\Local\npm-cache\_logs\2024-12-06T08_37_41_023Z-debug-0.log
npm install --no-audit --save @testing-library/jest-dom@^5.14.1 @testing-library/react@^13.0.0 @testing-library/user-event@^13.2.1 web-vitals@^2.1.0 failed


# 위 에러는 버전충돌 에러다 

rm -rf node_modules package-lock.json 명령어를 사용하는 이유는 의존성 관련 문제를 해결하기 위해입니다. 이 명령어는 프로젝트의 의존성 캐시와 잠금 파일을 삭제하여, 새로 설치할 때 의존성 충돌이나 문제가 발생하지 않도록 하기 위함


rm -rf node_modules package-lock.json
npm install



ERROR in ./src/reportWebVitals.js 5:4-24
Module not found: Error: Can't resolve 'web-vitals' in 'C:\VsCode\netplix2-front\netplix-front\src

이 에러는 web-vitals 패키지를 찾을 수 없다는 에러입니다. reportWebVitals.js 파일에서 web-vitals 라이브러리를 임포트하려고 했는데, 해당 라이브러리가 프로젝트에 설치되지 않은 경우 발생

해결방안 npm install web-vitals