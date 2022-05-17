pkgname="execute-process-linux"
pkgver=2.5
pkgrel=0
pkgdesc="advanced process execution static library"
author="imperzer0"
arch=("x86_64")
url="https://github.com/imperzer0/execute-process-linux"
license=('GPL3')
depends=()
makedepends=()

_srcprefix="local:/"
_libfiles=("execute-process-linux" "execute-process-linux-defs")

# add all library files to sources
for _libfile in ${_libfiles[@]}
{
    source=(${source[@]} "$_srcprefix/$_libfile")
}

# skip all checksums
for _libfile in ${_libfiles[@]}
{
    md5sums=(${md5sums} "SKIP")
}

package()
{
    for _libfile in ${_libfiles[@]}
	{
	    install -Dm755 "./$_libfile" "$pkgdir/usr/include/$_libfile"
	}
}
