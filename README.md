[Crystal][crystal] is a young compiled programming language that is similar to Ruby in
syntax but is much faster. It is non-trivial to install Crystal without the
root permision. Although you can find precompiled binary packages from Crystal's
release page, those packages lack essential libraries required to
compile any Crystal programs. As a result, users have to install additional
packages to make Crystal work.

This repository provides portable precompiled Crystal binaries. The only
difference from the official packages is that pacakges here include static
[libevent][libev] and [PCRE][pcre] libraries. Users can download a package from
the [release page][rel], unpack it and run
`crystal-verion_x64-linux/bin/crystal` to compile their programs without
installing other libraries. **More importantly**, executables
compiled with our binary distributions are not dynamically linked to the two
libraries and are thus more portable -- as developers, we wouldn't want our
users to install other libraries to use our tools.

At present, this repository does not provide libyaml and libgmp which are
required to compile certain crystal programs.

[crystal]: https://crystal-lang.org/
[libev]: https://libevent.org/
[pcre]: https://www.pcre.org/
[rel]: https://github.com/lh3/PortableCrystal/releases
