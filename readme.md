유튜브 클론코딩 오류 메세지

```
npm WARN youtube@1.0.0 No description
npm WARN optional SKIPPING OPTIONAL DEPENDENCY: fsevents@2.3.2 (node_modules\fsevents):
npm WARN notsup SKIPPING OPTIONAL DEPENDENCY: Unsupported platform for fsevents@2.3.2: wanted {"os":"darwin","arch":"any"} (current: {"os":"win32","arch":"x64"})

npm ERR! code EPERM
npm ERR! syscall rename
npm ERR! path C:\Users\000\Desktop\youtube\node_modules\is-bigint\package.json.3837146886
npm ERR! dest C:\Users\000\Desktop\youtube\node_modules\is-bigint\package.json
npm ERR! errno -4048
npm ERR! Error: EPERM: operation not permitted, rename 'C:\Users\000\Desktop\youtube\node_modules\is-bigint\package.json.3837146886' -> 'C:\Users\000\Desktop\youtube\node_modules\is-bigint\package.json'
npm ERR!  [OperationalError: EPERM: operation not permitted, rename 'C:\Users\000\Desktop\youtube\node_modules\is-bigint\package.json.3837146886' -> 'C:\Users\000\Desktop\youtube\node_modules\is-bigint\package.json'] {
npm ERR!   cause: [Error: EPERM: operation not permitted, rename 'C:\Users\000\Desktop\youtube\node_modules\is-bigint\package.json.3837146886' -> 'C:\Users\000\Desktop\youtube\node_modules\is-bigint\package.json'] {
npm ERR!     errno: -4048,
npm ERR!     code: 'EPERM',
npm ERR!     syscall: 'rename',
npm ERR!     path: 'C:\\Users\\000\\Desktop\\youtube\\node_modules\\is-bigint\\package.json.3837146886',
npm ERR!     dest: 'C:\\Users\\000\\Desktop\\youtube\\node_modules\\is-bigint\\package.json'
npm ERR!   },
npm ERR!   errno: -4048,
npm ERR!   code: 'EPERM',
npm ERR!   syscall: 'rename',
npm ERR!   path: 'C:\\Users\\000\\Desktop\\youtube\\node_modules\\is-bigint\\package.json.3837146886',
npm ERR!   dest: 'C:\\Users\\000\\Desktop\\youtube\\node_modules\\is-bigint\\package.json',
npm ERR!   parent: 'youtube'
or antivirus),
npm ERR! or that you lack permissions to access it.
npm ERR!
npm ERR! If you believe this might be a permissions issue, please double-check the
npm ERR! permissions of the file and its containing directories, or try running
npm ERR! the command again as root/Administrator.

npm ERR! A complete log of this run can be found in:
npm ERR!     C:\Users\000\AppData\Roaming\npm-cache\_logs\2021-10-09T02_36_41_559Z-debug.log
```

> 원인 : npm install @babel/core @babel/node --save-dev 명령어를 사용했을 때 발생하는 오류
> 에러 메세지 확인 : EPERM이 읽어들이지 못해서 오류가 발생함. 관리자 권환으로 다시 명령을 실행해보라고 함.
> 에러 메세지 의미 확인 : 

참고 링크 

https://plming.tistory.com/211
https://stackoverflow.com/questions/35023667/difference-between-eacces-and-eperm
https://stackoverflow.com/questions/45557788/npm-err-code-eperm

요약 : vs 코드에서 cli를 사용하여 npm을 못찾을 때 발생하는 오류이다. vs code를 닫고 다시 시작해서 사용하면 정상적으로 되는 경우도 존재함.

> 해결 방법 : npm i @babel/node --save-dev 으로 따로 설치 
