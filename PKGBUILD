# Maintainer: Vivien Maisonneuve <v dot maisonneuve at gmail dot com>
# Category: science
pkgname='polylib'
pkgver='5.22.5'
pkgrel=3
pkgdesc='A library of polyhedral functions'
arch=('i686' 'x86_64')
url='http://icps.u-strasbg.fr/polylib/'
license=('GPL3')
depends=('gmp')
source=("http://icps.u-strasbg.fr/polylib/polylib_src/polylib-$pkgver.tar.gz")
md5sums=('c0088786e0a5ae64b7cc47ad19ae4f83')

build() {
    cd "$srcdir/$pkgname-$pkgver"
    ./configure --prefix=/usr --with-libgmp
    make
}

check() {
    cd "$srcdir/$pkgname-$pkgver"
    make tests
}

package() {
    cd "$srcdir/$pkgname-$pkgver"
    make prefix="$pkgdir"/usr install
}
