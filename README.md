# ts-backend
```
실행 순서
1. 폴더생성
2. npm init
3. npm install typescript nodemon ts-node prettier
4. node_modules/.bin/tsc --init : tsconfig.json 파일 생성
 => 글로벌로 설치하면 tsc --init하면 되는듯
5. tsconfig파일의 outDir option을 ./build로 바꿔줌
6. package.json의 scripts의 build로 변경
    => "build": "rm -rf build/ && prettier --write source/ && tsc"
7. npm i express body-parser dotenv
8. npm i --save-dev @types/express @types/body-parser @types/dotenv
9. .prettierrc 생성
{
    "singleQuote": true,
    "printWidth": 200,
    "proseWrap": "always",
    "tabWidth": 4,
    "useTabs": false,
    "trailingComma": "none",
    "bracketSpacing": true,
    "jsxBracketSameLine": false,
    "semi": true
}
10. settings.json 생성
{
    "editor.defaultFormatter": "esbenp.prettier-vscode",
    "[javascript]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "[typescript]": {
        "editor.formatOnSave": true,
        "editor.formatOnPaste": true
    },
    "[markdown]": {
        "editor.formatOnSave": true,
        "editor.wordWrap": "on",
        "editor.renderWhitespace": "all",
        "editor.acceptSuggestionOnEnter": "off"
    }
}
11. logging.ts 작성
12. config.ts 작성
13. server.ts 생성
14. controller 폴더 생성
15. routes 폴더 생성
16. server.ts에 route basic경로 생성 및 import
17. npm run build


-----------  mongodb  -------------
18. npm i mongoose
19. npm i --save-dev @types/mongoose
20. config.ts에 mongo connection option을 넣어줌
const MONGO_OPRIONS = {
    useUnifiedTopology: true,
    useNewUrlParser: true,
    socketTimeoutMS: 30000,
    keepAlive: true,
    poolSize: 50,
    autoIndex: false,
    retryWrites: false
};
21. mongodb 사용 설정
22. monggose connect(url, oprtions) in server.ts 
23. interfaces 작성
24. Schema in models 작성

* 실행 nodemon source/server.ts
```