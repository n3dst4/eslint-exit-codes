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
