# Great eslint config

```javascript
module.exports = {
  env: {
    browser: true,
    es6: true
  },
  extends: ['eslint:recommended', 'plugin:react/recommended', 'plugin:flowtype/recommended'],
  parser: 'babel-eslint',
  parserOptions: {
    ecmaFeatures: {
      experimentalObjectRestSpread: true,
      jsx: true
    },
    sourceType: 'module'
  },
  plugins: [
    'react',
    'flowtype',
    'import',
  ],
  globals: {
    'Urls': true,
    '__DEBUG__': true,
    '__INITIAL_STATE__': true,
    '__ENV__': true,
    'CACHE_BUST': true,
    'require': true,
    // Flow types
    'Method': true,
  },
  rules: {
    indent: [
      'error',
      2,
      {"SwitchCase": 1}
    ],
    "react/self-closing-comp": ["error", {
    "component": true,
    "html": true
    }],
    "keyword-spacing": ["error", {
      "before": true,
      "after": true,
    }],
    'linebreak-style': [
      'error',
      'unix'
    ],
    quotes: [
      'error',
      'single'
    ],
    'no-extra-semi': [
      'error',
    ],
    'comma-dangle': [
      'error',
      'always-multiline'
    ],
    'no-console': [
      'error',
      {allow: ["info", "warn", "error", "trace"]}
    ],
    'no-unused-vars': [
      'error',
      {varsIgnorePattern: 'ignored', argsIgnorePattern: 'ignored'},
    ],
    'no-multi-spaces': 'error',
    'curly': 2,
    'dot-notation': 2,
    'dot-location': [2, 'property'],
    eqeqeq: [2, 'smart'],
    'no-alert': 2,
    'no-caller': 2,
    'no-implicit-coercion': 2,
    'no-implicit-globals': 2,
    'no-trailing-spaces': ['error', {skipBlankLines: false}],
    'no-whitespace-before-property': 'error',
    'space-before-blocks': 'error',
    'space-before-function-paren': ['error', 'never'],
    'space-in-parens': ['error', 'never'],
    'space-infix-ops': 'error',
    'space-unary-ops': ['error', {
      words: true,
      nonwords: false,
    }],
    // It is annoying to add the parens when changing the signature from
    // single to multiple args so enforce parens at all time.
    'arrow-parens': ['error', 'as-needed'],
    'import/no-duplicates': 'error',
    'react/prop-types': [2, {ignore: ['children']}],
    'object-curly-spacing': ['error', 'never'],
    'eol-last': 'error',
    'block-spacing': ['error', 'never'],
    'no-multiple-empty-lines': ['error', {max: 2, maxEOF: 1}],
    'no-irregular-whitespace': ['error', {skipRegExps: true, skipTemplates: true, skipStrings: true}]
  }
};

```
