# @kasanie_laski/linters

Shared **ESLint**, **Stylelint** and **Prettier** flat-config presets for React + `styled-components` projects (TypeScript-ready).

## Requirements

Peer dependencies you must have installed in your project:

| Package      | Version          |
| ------------ | ---------------- |
| `eslint`     | `^9.23.0`        |
| `stylelint`  | `^16.16.0`       |
| `prettier`   | `^3.5.3`         |
| `typescript` | `>=4.8.4 <5.9.0` |

## Install

```bash
npm install --save-dev @kasanie_laski/linters eslint stylelint prettier typescript
```

## Usage

### ESLint

`eslint.config.js`:

```js
import { eslint } from '@kasanie_laski/linters';

export default eslint;
```

Covers: `eslint:recommended`, `plugin:react/recommended`, `plugin:@typescript-eslint/recommended`, `plugin:react-hooks/recommended`, `plugin:jsx-a11y/recommended`, plus `eslint-plugin-prettier` integration.

### Stylelint

`stylelint.config.js`:

```js
import { styleLint } from '@kasanie_laski/linters';

export default styleLint;
```

Extends `stylelint-config-standard` + `stylelint-config-recess-order` (property ordering), and parses CSS-in-JS via `postcss-styled-syntax`.

### Prettier

`prettier.config.js`:

```js
import { prettier } from '@kasanie_laski/linters';

export default prettier;
```

## Scripts

Add to your `package.json`:

```json
{
  "scripts": {
    "lint": "eslint \"{src,lib,services}/**/*.{js,ts,jsx,tsx}\"",
    "lint:css": "stylelint \"{src,lib,services}/**/*.{jsx,tsx,ts,js}\"",
    "format": "prettier --write \"{src,lib,services}/**/*.{js,ts,tsx,jsx,json,md}\""
  }
}
```

## VS Code

Install the [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint), [Stylelint](https://marketplace.visualstudio.com/items?itemName=stylelint.vscode-stylelint) and [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) extensions so the rules above are enforced and auto-fixed on save.

## License

ISC
