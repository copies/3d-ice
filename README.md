# 3D-ICE

Hosting for [3D-ICE][1]. Refer to the original [README](README) for further
details.

## Compilation

The library has been developed using `bison 2.4.1`, and it is not compatible
with newer versions. Patching is required as shown below.

```shell
curl https://raw.githubusercontent.com/copies/3d-ice/patches/v2.2.5.patch | git apply
```

[1]: http://esl.epfl.ch/3d-ice
