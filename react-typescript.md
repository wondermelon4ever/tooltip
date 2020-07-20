1. npm init
2. npm install --save react react-dom
3. npm install --save @types/react @types/react-dom
4. npm install --save-dev typescript
5. npm install --save-dev tsloader
6. npx typescript --init
7. edit webpack.config.js   
   module.exports = {
     mode: 'development',  
  
     // 엔트리 포인트   
     entry: "./src/index.tsx",  

     // 빌드 결과물을 dist/main.js에 위치  
     output: {  
       filename: "main.js",  
       path: __dirname + "/dist"  
     },  
  
     // 디버깅을 위해 빌드 결과물에 소스맵 추가  
     devtool: "source-map",  
  
     resolve: {  
       // 파일 확장자 처리  
       extensions: [".ts", ".tsx", '.js']  
    },  
  
  module: {  
    rules: [  
      // .ts나 .tsx 확장자를 ts-loader가 트랜스파일   
      { test: /\.tsx?$/, loader: "ts-loader" },  
    ]  
  },  
};  
   
  
reference: http://jeonghwan-kim.github.io/dev/2019/06/25/react-ts.html
