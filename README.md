# Configurations!

### Eslint
 ```
	   yarn add eslint-plugin-import-helpers eslint-import-resolver-typescript @eslint/eslintrc eslint-plugin-react -D
```
 ### eslint.config.cjs
 ```
 // eslint-disable-next-line @typescript-eslint/no-require-imports

const { FlatCompat } =  require('@eslint/eslintrc')

  

const compat =  new  FlatCompat({

baseDirectory: __dirname,

})

  

module.exports  = [

...compat.plugins('react'),

...compat.config({

plugins: ['react', '@typescript-eslint', 'eslint-plugin-import-helpers', 'prettier'],

extends: [

'plugin:react/recommended',

'plugin:@typescript-eslint/recommended',

'prettier',

'plugin:prettier/recommended',

],

env: {

es2020:  true,

node:  true,

},

rules: { 'react/react-in-jsx-scope':  'off' },

}),

]
 ```
## Prettier
  ```
	   yarn add prettier eslint-config-prettier eslint-plugin-prettier -D
```
 ### .prettierrc.json
 ```
{

"trailingComma":  "es5",

"tabWidth":  4,

"semi":  false,

"endOfLine":  "auto",

"printWidth":  100,

"singleQuote":  true,

"jsxSingleQuote":  true,

"bracketSpacing":  true,

"arrowParens":  "avoid",

"proseWrap":  "preserve",

"htmlWhitespaceSensitivity":  "css",

"embeddedLanguageFormatting":  "auto"

}
```
