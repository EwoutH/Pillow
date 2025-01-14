README
------

This directory creates wheels for tagged versions of Pillow.

Archives
--------

https://github.com/python-pillow/pillow-depends contains archives for libraries
that will be built as part of the Pillow build.

In general, there is no need to put library archives there, because the
`multibuild` scripts will download them from their respective URLs.

But, the build will look in that repository before downloading from the
URL, so if there is a library that often fails to download, or you think might
fail to download, then download it and add it to the Git repository.

See the `pre_build` in `config.sh` and the `fetch_unpack` routine in
`multibuild/common_utils.sh` for the logic, and the build recipes in
`multibuild/library_builders.sh` for the filename to give to the downloaded
archive.

Wheels
------

Wheels are
[GitHub Actions artifacts created for tags, relevant changes or manual builds](https://github.com/python-pillow/Pillow/actions/workflows/wheels.yml).

Windows wheels are not created here. Instead, they are
[GitHub Actions artifacts created on each run of the Windows workflow](https://github.com/python-pillow/Pillow/actions/workflows/test-windows.yml?query=branch%3Amain).
