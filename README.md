Reproducer of an issue where `pixi-build` doesn't use a target's specific build dependency when cross-compiling for this target.

When cross-compiling for `osx-arm64`, one currently needs the `sigtool` dependency. If it is included in the `package.build-dependencies` the build works, but if it is included in `package.target.osx-64.build-dependencies` the dependency is not used and the build fails with an error `codesign` not found.

```sh
# works with `sigtool` in `package.build-dependencies` but not with `package.target.osx-64.build-dependencies`
SDKROOT=/path/to/MacOSX11.0.sdk/ pixi build --target-platform=osx-arm64
```
