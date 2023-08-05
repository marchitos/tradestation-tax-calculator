- creare progetto
    git init
    pnpm init (why pnpm?)
    pnpm add -D typescript @types/node
    pnpm tsc --init
    mkdir src
    touch src/index.ts
    echo "node_modules" > .gitignore

    pnpm add -D tsup

    package json script -> build: "tsup src/index.ts --format cjs,esm --dts"

    BONUS - test vitest
    pnpm add -D vitest
    index.test.ts -> add code
    package json scripts -> dev, test

- creare build automatica
    add github actions folder
    add main yaml file
    add ci script to package json -> "ci": 
    