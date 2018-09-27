# Contributor: Cody Schafer <alpine@codyps.com>
# Maintainer: Cody Schafer <alpine@codyps.com>
pkgname=gcc-arm-embedded-bin
pkgver=7.2018.2
pkgrel=0
pkgdesc="GNU Tools ARM Embedded Processors (binary distribution, includes newlib, does NOT include GDB)"
url="https://developer.arm.com/open-source/gnu-toolchain/gnu-rm"
arch="x86_64"
license="custom"
depends="libgcc glibc"
depends_dev=""
makedepends="$depends_dev"
install=""
subpackages="$pkgname-dev $pkgname-doc"

_ver_major="${pkgver%%.*}"
_ver_rem1="${pkgver#*.}"
_ver_year="${_ver_rem1%%.*}"
_ver_q="q${_ver_rem1#*.}"
_ver_kind="update"
 source="https://armkeil.blob.core.windows.net/developer/Files/downloads/gnu-rm/${_ver_major}-${_ver_year}${_ver_q}/gcc-arm-none-eabi-${_ver_major}-${_ver_year}-${_ver_q}-${_ver_kind}-linux.tar.bz2"

sha512sums="052ea750631675d6b7a005d0cdb8eca7db73b600165f7a3f3c52e46764e7729b6aa5efd2b90ff1f81e4d22314cbdfae1e02ebd39808c3223052ca8de756dbd46  gcc-arm-none-eabi-7-2018-q2-update-linux.tar.bz2"
md5sums="299ebd3f1c2c90930d28ab82e5d8d6c0  gcc-arm-none-eabi-7-2018-q2-update-linux.tar.bz2"
# gcc-arm-none-eabi-7-2018-q2-update
builddir="$srcdir/gcc-arm-none-eabi-${_ver_major}-${_ver_year}-${_ver_q}-${_ver_kind}"

build() {
	cd "$builddir"
}

check() {
	cd "$builddir"
}

package() {
	cd "$builddir"
	mkdir -p $pkgdir/usr
	cd $srcdir/gcc-*/
	cp -a * $pkgdir/usr
	rm -f $pkgdir/usr/bin/arm-none-eabi-gdb*
	rm -f $pkgdir/usr/lib/libcc1.so*
}

