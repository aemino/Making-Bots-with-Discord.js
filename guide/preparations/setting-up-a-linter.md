## Preparing a better development environment

As a developer, it's a good idea to make your development process as streamlined as possible. Installing and utilizing the right tools is an essential part of any project you're working on. Although it's not required, installing a linter will help you greatly.

### Installing a code editor

First, you will need a proper code editor. Using Notepad and Notepad++ is discouraged, as they're inefficient for projects like these. If you are using either, it is highly recommended to switch in order to save everyone lots of headaches and unnecessary syntax error questions.

* [Visual Studio Code](https://code.visualstudio.com/) is a very popular choice known for being fast and powerful. It supports a broad range of languages and comes with its own terminal, as well as built-in intellisense and autocomplete for both JavaScript and TypeScript. This is the recommended choice.
* [Atom](https://atom.io/) is user-friendly, being concise and easy to navigate. This is what many developers use to get started.
* [Sublime Text](https://www.sublimetext.com/) is another powerful editor known for looking sleek and performing speedily and efficiently.

### Installing a linter

One of the major advantages proper code editors have over Notepad and Notepad++ is their ability to use linters. Linters check syntax and help you produce consistent code that follows certain style rules that you can define yourself, if you choose to do so. They help form good habits if you stick to a single configuration. When you start using a linter, you might be bombarded with errors at first. This is normal and perfectly fine. It might be a pain to get through during the initial process, but it's most definitely worth it.

* [ESLint for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
* [ESLint for Atom](https://atom.io/packages/eslint)
* [ESLint for Sublime Text](https://packagecontrol.io/packages/ESLint)

<p class="tip">You can install each of these directly inside the editors themselves. For Visual Studio Code, press `Ctrl + Shift + X`. For Atom, press `Ctrl + ,` and click on "Install". For Sublime, press `Ctrl + Shift + P` and search for "Install Package" (available via [Package Control](https://packagecontrol.io/installation)). After that, you may then search for "eslint" and install it through there.</p>

### Setting up ESLint rules

ESLint may display a lot of warnings and errors about your code when you start using it, but don't let this startle you. In order to get started, follow these steps:

1. Create a file in your root directory named `.eslintrc.json` (where your main project file is located).
2. Copy the code below into the file.

```json
{
	"extends": "eslint:recommended",
	"env": {
		"node": true,
		"es6": true
	},
	"parserOptions": {
		"ecmaVersion": 2017
	},
	"rules": {
		"brace-style": ["error", "stroustrup", { "allowSingleLine": true }],
		"comma-dangle": ["error", "always-multiline"],
		"comma-spacing": "error",
		"comma-style": "error",
		"curly": ["error", "multi-line", "consistent"],
		"dot-location": ["error", "property"],
		"handle-callback-err": "off",
		"indent": ["error", "tab"],
		"max-nested-callbacks": ["error", { "max": 4 }],
		"max-statements-per-line": ["error", { "max": 2 }],
		"no-console": "off",
		"no-empty-function": "error",
		"no-floating-decimal": "error",
		"no-inline-comments": "error",
		"no-lonely-if": "error",
		"no-multi-spaces": "error",
		"no-multiple-empty-lines": ["error", { "max": 2, "maxEOF": 1, "maxBOF": 0 }],
		"no-shadow": ["error", { "allow": ["err", "resolve", "reject"] }],
		"no-trailing-spaces": ["error", { "skipBlankLines": true }],
		"no-var": "error",
		"object-curly-spacing": ["error", "always"],
		"prefer-const": "error",
		"quotes": ["error", "single"],
		"semi": ["error", "always"],
		"space-before-blocks": "error",
		"space-before-function-paren": ["error", "never"],
		"space-in-parens": "error",
		"space-infix-ops": "error",
		"space-unary-ops": "error",
		"spaced-comment": "error",
		"yoda": "error"
	}
}
```

The major points of this setup would be:

* Allowing you to debug with `console.log()`;
* Prefer using `const` over `let` or `var`, as well as disallow `var`;
* Disapproving of variables with the same name in callbacks;
* Requiring semicolons. While it's not required in JavaScript, it's considered one of the most common best practices to follow;
* Requiring accessing properties to be on the same line;
* Requiring indenting to be done with tabs;
* Limiting nested callbacks to 4. If you hit this error, it is a good idea to consider refactoring your code.

If your current code style is a bit different or you simply don't like a few of these rules, that's perfectly fine! Just head over the the [ESLint docs](https://eslint.org/docs/rules/), find the rule(s) you want to modify, and change them accordingly.
