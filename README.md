# learn-nodejs-typescript
A project to learn writing nodejs code using typescript language

## Package installed

```sh
npm i -D typescript nodemon ts-node @types/node 
```

## Info
- To start with, so that we can start writing code in ts file create `tsconfi.js` file in the root folder as below

```json
// tsconfig.json
{
    "compilerOptions": {
        "target": "ES5",
        "moduleResolution": "node",
        "module": "commonjs",
        "sourceMap": true,
        "outDir": "dist",
        "lib": [
            "ESNext"
        ]
    }
}
```

- Next we will use nodemon to keep a watch on the ts file inside src folder and delegate the execution to ts-node
- So create a `nodemon.json` file in root folder 

```json
// nodemon.json
{
    "watch": "src/**/*.ts",
    "execMap": {
        "ts": "./node_modules/.bin/ts-node"
    }
}
```

- Ts Node will transform the ts into js and execute on NodeJs
- Update the package.json>scripts to have `start: nodemon src/index.ts`
- Next you can open terminal and run `npm start`
- For further learnings follow `tutorials` folder. I will udpate it as my learning continues.