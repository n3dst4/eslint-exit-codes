Minimal demo of ESLint exiting with nonzero exit codes if any warnings are found.

Assuming you have nodejs installed (https://nodejs.org/en/):

```sh
cd eslint-exit-codes
npm install
```

will install eslint locally in this folder.


```sh
npm run good
```

Will run eslint on a file with no warnings

```sh
npm run bad
```

will run eslint on a file with a couple of warnings. Npm will complain loudly about the exit code.

If you open `bad.js` in Emacs with `flycheck` and `add-node-modules-path`, eslint will run but complain with:

```
Suspicious state from syntax checker javascript-eslint: Flycheck checker javascript-eslint returned non-zero exit code 1, but its output contained no errors: <?xml version="1.0" encoding="utf-8"?><checkstyle version="4.3"><file name="c:/git/eslintfu/good.js"><error line="4" column="1" severity="error" message="Too many blank lines at the end of file. Max of 0 allowed. (no-multiple-empty-lines)" source="eslint.rules.no-multiple-empty-lines" /></file></checkstyle>

Try installing a more recent version of javascript-eslint, and please open a bug report if the issue persists in the latest release.  Thanks!

```

You can replicate this again by opening `good.js` (no errors) and breaking it in some way.
