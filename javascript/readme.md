# JavaScript

1. [Yarn](https://yarnpkg.com/) **(Preferred over NPM)**

2. [ESLint](https://eslint.org/) _(Config below)_

3. [Prettier with ESLint](https://prettier.io/docs/en/eslint.html) _(Config below)_

4. [Stylelint](https://stylelint.io/)

5. [Vue JS](https://vuejs.org)

### ESLint Config

`.eslintrc`
```
{
  "env": {
    "browser": true,
    "commonjs": true,
    "es6": true,
    "node": true
  },
  "extends": [
    "eslint:recommended",
    "plugin:vue/recommended",
    "plugin:prettier/recommended"
  ],
  "parser": "vue-eslint-parser",
  "parserOptions": {
    "parser": "babel-eslint",
    "sourceType": "module"
  },
  "plugins": [
    "prettier"
  ],
  "rules": {
    "vue/v-on-style": ["error", "longform"],
    "vue/v-bind-style": ["error", "longform"],
    "vue/name-property-casing": ["error", "kebab-case"],
    "vue/max-attributes-per-line": ["error", {
      "singleline": 20,
      "multiline": {
        "max": 1,
        "allowFirstLine": false
      }
    }]
  }
}
```

### Prettier Config

`.prettierrc`
```
{
  "arrowParens": "always",
  "printWidth": 120,
  "semi": false
}
```

### Stylelint Config

`.stylelintrc`
```
{
  "extends": "stylelint-config-standard",
  "rules": {
    "string-quotes": "double",
    "declaration-empty-line-before": null
  }
}
```
