1. Initialize Node Package Manager
   package.json -> npm init
   
2. Changes in package.json
   type: module
   main: bella.js
   
3. Initialize Typescript Configuration
   tsconfig.json -> tsc init
   
4. Changes in tsconfig.json
   target: esnext
   module: esnext
   
5. Compile typescript to javascript
   tsc --watch (bella.ts -> bella.js)
   
6. Run node bella.js
   node bella.js (OUTPUT)
