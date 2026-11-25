# npbuild

A shell script for building library packages and non-locatable packages for host, which is used by [ndk-pkg](https://github.com/leleliu008/ndk-pkg), [ppkg](https://github.com/leleliu008/ppkg), [xcpkg](https://github.com/leleliu008/xcpkg)

## Influential environment variables

`CC`, `AR`, `RANLIB`, `CFLAGS`, `CPPFLAGS`, `LDFLAGS`

## Usage

```bash
./npbuild [options] <PACKAGE-NAME>...

    <PACKAGE-NAME> can be any one of libz, libiconv, libxml2, libexpat, libtool, itstool, intltool, texinfo, help2man, automake, autoconf, autoconf_archive, netsurf_buildsystem, perl_XML_Parser

    options:

       -j <N>
            specify the number of jobs you can run in parallel.

       --uppm <FILEPATH>
            specify the path of uppm executable.

       --urlmap <FILEPATH>
            specify the path of urlmap executable.

       --prefix <DIR>
            specify the directory where files should be installed. default to ~/.fpliu/native/

       --download-dir <DIR>
            specify the directory where source files should be downloaded. default to ~/.fpliu/downloads/

       --session-dir <DIR>
            specify the directory where source files should be uncompressed. default to ~/.fpliu/run/$$
```
