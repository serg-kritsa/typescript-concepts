npm i typescript -g
## compile ts file
cd ./basics/00-compilation/
npm i
.\node_modules\.bin\tsc .\using-ts.ts
### compile in watch mode
.\node_modules\.bin\tsc .\using-ts.ts --watch
    OR .\node_modules\.bin\tsc .\using-ts.ts -w

## compile the entire project
tsc --init
`tsc` OR `tsc --watch` OR `tsc -w`

## Include files
"include": []
"files": []

## Exclude files
"node_modules" would be excluded the default
"*.dev.ts" would be excluded with specified ending
"**/*.dev.ts" would be excluded with specified ending anywhere

## Compilation options
[https://www.typescriptlang.org/docs/handbook/tsconfig-json.html]
[https://www.typescriptlang.org/docs/handbook/compiler-options.html]
compilerOptions.target: es5 to support execution in old browsers 
"lib": [ "DOM", "DOM.Iterable", "ES6", "ScriptHost" ],     default libs if not specified
"sourceMap": true,      useful to simplify debugging
"outDir": "./dist",     folder for compiled files      
"rootDir": "./src",     folder w/ ts files to be compiled
"removeComments": true, useful to make output smaller        
"noEmit": true,         don't generate js files. useful for finding errors
"noEmitOnError": true,  no files will be emitted if there is error

## run a lite server
* npm i lite-server -D
* add line to package.json `"scripts": { "start": "lite-server" },`
* npm run start

## debug the ts app
install `Debugger for Microsoft Edge` extention
    edit launch.json file
npm i
    enable sourceMap in tsconfig.json using `"sourceMap": true,`    
    npm run ts
    npm run start
set breakpoint in ts file
press F5 to start
see console messages in `DEBUG CONSOLE` tab not `TERMINAL`

## know es6 support in browsers
[https://kangax.github.io/compat-table/es6/]

## use reference value
[https://academind.com/tutorials/reference-vs-primitive-values/]

## write a class
[https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes/Public_class_fields]
[https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain]

## use an interface
interface will not appear in compiled js and is only needed for development.

## enable decorator in tsconfig
,"experimentalDecorators": true,        /* Enables experimental support for ES7 decorators. */

## HTML Drag and Drop API Documentation on MDN 
[https://developer.mozilla.org/en-US/docs/Web/API/HTML_Drag_and_Drop_API](HTML Drag and Drop API)

## google geocoding api
[https://developers.google.com/maps/documentation/geocoding/start?hl=ru]
[https://developers.google.com/maps/documentation/javascript/overview?hl=ru]

## NodeJS & TS
(1st terminal) tsc -w
(2nd terminal) npm start

### CRUD 
Routes could be tested in Postman 