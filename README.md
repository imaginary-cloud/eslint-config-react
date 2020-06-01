# eslint-config-react
ESLint configuration for React Project. Easy to install and configure, it follows the best code standards from airbnb and uses prettier configuration on code format. Integrated with our [prettier configuration](https://github.com/imaginary-cloud/prettier-config) configuration

## Purpose
This configuration uses airbnb and Prettier configuration plus some extra rules that we find handy for *React* applications

For more information you can check [ESLint](https://eslint.org/) and [Prettier](https://prettier.io/) documentations as well the [airbnb](https://github.com/airbnb/javascript/tree/master/packages/eslint-config-airbnb) and [prettier](https://github.com/prettier/eslint-config-prettier) configurations for more information

This package integrates the Prettier rules with ESLint using our configuration. You can check it at [@imaginary-cloud/prettier-configuration](https://github.com/imaginary-cloud/prettier-config)

## How to install
You need ESLint and Prettier installed as development dependencies on your project. You can install them by using **npm** or **yarn**.

#### NPM

```
npm install --save-dev eslint prettier
```

Install all peer dependencies of our configuration, these can be listed by the command:
```
npm info "@imaginary-cloud/eslint-config-react@latest" peerDependencies
```

If running *npm > v5* you install them by:
```
npx install-peerdeps --dev @imaginary-cloud/eslint-config-react
```

If *npm < v5*, Linux/OSX users can run:
```
(
  export PKG=@imaginary-cloud/eslint-config-react;
  npm info "$PKG@latest" peerDependencies --json | command sed 's/[\{\},]//g ; s/: /@/g' | xargs npm install --save-dev "$PKG@latest"
)
```

#### YARN

```
yarn add eslint prettier -D
```

Install the peer dependencies tool, by running:
```
yarn global add install-peerdeps
```

and after that run the following command to install the project's config:
```
install-peerdeps @imaginary-cloud/eslint-config-react
```

## How to use
To configure ESLinter and Prettier you can add to your `package.json`
```
"eslintConfig": {
  "extends": "@imaginary-cloud/react",
},
"prettier": "@imaginary-cloud/prettier-config"
```

Or create a `.eslintrc` and `.prettierrc` files and add `extends: "@imaginary-cloud/react"` and `"@imaginary-cloud/prettier-config"` respectivally. As an example:
```
<!-- .eslintrc -->
{
  "extends": "@imaginary-cloud/react"
  <!-- you can edit this configuration as usual, check ESLint docs -->
}

<!-- .prettierrc -->
"@imaginary-cloud/prettier-config"
```

To use ESLint and Prettier you can add this scripts to your `package.json` file
```
"lint": "eslint ./ --ignore-path .gitignore",
"lint:fix": "npm run lint -- --fix",
"format": "prettier --write \"{,!(node_modules)/**/}*.js\""
```

## Contributing
How to [contribute](/CONTRIBUTING.MD) to this open source library

## License

Copyright © 2010-2020 [Imaginary Cloud](https://www.imaginarycloud.com/?utm_source=github). This library is licensed under the MIT [license](/LICENCE).

## About Imaginary Cloud

[![Imaginary Cloud](https://s3.eu-central-1.amazonaws.com/imaginary-images/Logo_IC_readme.svg)](https://www.imaginarycloud.com/?utm_source=github)

At Imaginary Cloud, we build world-class web & mobile apps. Our Front-end developers and UI/UX designers are ready to create or scale your digital product. Take a look at our [website](https://www.imaginarycloud.com/?utm_source=github) and [get in touch!](https://www.imaginarycloud.com/contacts/?utm_source=github) We'll take it from there.
