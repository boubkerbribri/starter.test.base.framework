#### Step 1
Init the project

```shell
npm init
```

#### Step 2
Install `prestashop_corp_tests_base_framework` with :

```shell
yarn add prestashop_corp_tests_base_framework
```

#### Step 3
Add `.gitignore`

```
node-modules
.idea
```

#### Step 4
Install typescript dependencies : 
```shell
yarn add -D typescript ts-node
```

-> Add `tsconfig.json` file

#### Step 5
Install ESLint dependencies : 
```shell
yarn add -D eslint eslint-config-prettier eslint-import-resolver-typescript eslint-plugin-import eslint-plugin-prettier
yarn add -D @typescript-eslint/eslint-plugin @typescript-eslint/parser @typescript-eslint/typescript-estree
```

Install Prettier :
```shell
yarn add -D prettier
```

Add ESLint file config -> `.eslintrc` 

Add Prettier file config -> `.prettierrc`

Add scripts for eslint on package.json:
```json
{
  "scripts": {
    "lint": "eslint . --ext .ts",
    "lint:fix": "eslint . --ext .ts --fix"
  }
}
```

#### Step 6
Create folders architecture : 

- `Test_Folder`
  - `campaigns`
    - `smoke`
    - `sanity`
    - `regression`
    - `...`
    - `helpers`
      - `mocha`
      - `routes`
  - `data`
    - `fixture`
    - `faker`
  - `pages`
    - `basePage.ts` -> Extends `CommonPage` form lib
      - `login`
      - `signUp`
  - `...`

#### Step 7
Install Mocha and Chai dependencies
```shell
yarn add mocha chai mochawesome
```

Add `.mocharc.json` file
