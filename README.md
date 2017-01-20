<!--
[![Build Status](https://travis-ci.org/YOUR_USERNAME/REPO_NAME.svg?branch=master)](https://travis-ci.org/USERNAME/REPONAME)
-->

# Angular Lib Seed

A basic boilerplate project for development of Angular library, mostly for personal projects.

# How to use?

## Library

To build the library:

```
$ npm run build
```

This script will:

1. Clean the `dist` directory.
2. Build the library to ES5 with ES2015 modules.
3. Create a UMD bundle with rollup.
4. Copy the `package.json` file and clean it up (drop `devDependencies`, `scripts`).
5. Generate metadata.
6. Copy the `README.md` file to `dist`.

To test the library use:

```
$ npm t
```

You can write tests in TypeScript and they will be run by mocha, with chai.

### TODO

- [ ] Support of test watch.

## Demo app

There are also boilerplates for a sample demo application. In order to build it use:

```
# A shell script
$ ./build-demo
```

The demo app is really, very simple and doesn't aim to do anything complicated. What the build script will do is:

1. Clean `demo/vendor`.
2. Copy each registered dependency of the demo app to `demo/vendor`.
3. Run `npm run build`.
4. Run `npm run build.demo` which will:
    1. Clean `demo/dist`.
    2. Compile the files from `demo/src`.
5. Copy `dist/*` to `demo/dist`.

In order to see your app:

```
$ cd demo && http-server .
```

# Demo

A project which uses this seed is [`ngresizable`](https://github.com/mgechev/ngresizable).

# License

MIT

