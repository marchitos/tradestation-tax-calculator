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

- creare build automatica