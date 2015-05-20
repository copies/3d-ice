# 3D-ICE

Hosting for [3D-ICE][1]. Refer to the original [README](README) for further
details.

## Compilation

The library has been developed using `bison 2.4.1`, and it is not compatible
with newer versions of `bison`. Patching is required as shown below.

```shell
curl https://raw.githubusercontent.com/copies/3d-ice/patches/v2.2.5-01-new-bison.patch | git apply
```

In addition, the parsing part of the library is not thread safe. Therefore,
calling the library from multiple threads might lead to data races. Patching is
required as shown below.

```shell
curl https://raw.githubusercontent.com/copies/3d-ice/patches/v2.2.5-02-reentrant-bison.patch | git apply
```

[1]: http://esl.epfl.ch/3d-ice
