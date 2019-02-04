# Build dcurl with bazel

This is a WIP and only support `BUILD_SSE` and `BUILD_AVX` at the moment. Please explicitly specify your option when building with bazel. By default, dcurl would build with SSE if no conditions specify.

### Default:

```
bazel build //src:dcurl
```

### AVX:

```
bazel --define BUILD_AVX=1 build //src:dcurl
```

### Debug:

```
bazel --define BUILD_DEBUG=1 build //src:dcurl
```

### Output:

```
./bazel-bin/src/dcurl.a
./bazel-bin/src/dcurl.so
```

## Testing

Explicitly specify options is still needed. For example:
```
bazel test --define BUILD_AVX //tests:pow
```

## TODO

* `BUILD_GPU`
* `BUILD_JNI`
* `BUILD_COMPAT`
* `BUILD_STAT`
* `BUILD_FPGA_ACCEL`
