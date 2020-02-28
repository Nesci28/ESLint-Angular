# ESLint-Angular
__How to add ESLint AirBnB to an Angular project__

### Install
```bash
yarn add -D eslint eslint-config-prettier eslint-plugin-import eslint-config-airbnb-angular @typescript-eslint/eslint-plugin @typescript-eslint/parser

npm install --save-dev eslint eslint-config-prettier eslint-plugin-import eslint-config-airbnb-angular @typescript-eslint/eslint-plugin @typescript-eslint/parser
```

### Configurations
__Create those files in the root folder of the project__

.eslintrc
```json
{
  "extends": ["airbnb-angular", "prettier"],
  "plugins": ["prettier"],
  "rules": {
    "prettier/prettier": ["error"],

    "import/extensions": [
      "error",
      "ignorePackages",
      {
        "js": "never",
        "jsx": "never",
        "ts": "never",
        "tsx": "never"
      }
    ]
  }
}
```

.prettierrc
```json
{
  "printWidth": 100,
  "singleQuote": true
}
```

package.json
```json
{
  "scripts": {
    "lint:fix": "eslint 'src/**/*.ts' --fix",
    "lint:check": "eslint 'src/**/*.ts'"
  }
}
```


