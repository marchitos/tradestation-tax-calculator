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
    add ci script to package json -> "ci": "pnpm run lint && pnpm run test && pnpm run build"
    set correct entries for files
        "main": "./dist/index.js",
        "module": "./dist/index.esm.js",
        "types": "./dist/index.d.ts",
    
    set npm package name and initial version
    create an npm token
    register npm token in github in settings -> Secrets and Variables -> Actions -> Repository Secrets

    add changeset
        pnpm add @changesets/cli -D
    init changeset
        pnpm changeset init
    add publish.yml
    verify to set "private":false in package.json
    verify to set "access": "public" in changeset config
    add release script -> "release": "pnpm run lint && pnpm run test && pnpm run build && changeset publish"

    run pnpm changeset for an "Initial commit"    