pkgname="execute-process-linux"
epoch=2
pkgver=4
pkgrel=0
pkgdesc="advanced process execution static library"
arch=("x86_64")
url="https://github.com/imperzer0/execute-process-linux"
license=('GPL')
# depends=()
makedepends=("cmake>=3.0")

libfiles=("execute-process-linux" "execute-process-linux-defs")

# add all library files to sources
for libfile in ${libfiles[@]}
{
    source=(${source[@]} "local://"$libfile)
}

# skip all checksums
for libfile in ${libfiles[@]}
{
    md5sums=(${md5sums} "SKIP")
}

# install=log-console.install

package()
{
    for libfile in ${libfiles[@]}
	{
	    install -Dm755 "./$libfile" "$pkgdir/usr/include/$libfile"
	}
}
