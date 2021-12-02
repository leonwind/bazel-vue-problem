# Bazel Vue.js problem

Minimal example of bazel not being able to serve vue.js. 
See [#3104](https://github.com/bazelbuild/rules_nodejs/issues/3104) for reference.

## How to reproduce
Working: `bazel build frontend:build` 

Failing: `bazel run frontend:serve` with the output 
```
ERROR  Failed to compile with 1 error

This relative module was not found:

* ./src/main.js in multi (webpack)-dev-server/client?http://10.46.16.83:8080&sockPath=/sockjs-node (webpack)/hot/dev-server.js ./src/main.js
```
