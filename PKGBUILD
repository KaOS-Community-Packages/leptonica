pkgname=leptonica
pkgver=1.72
pkgrel=1
pkgdesc="Library for image processing and image analysis"
arch=('x86_64')
url="http://www.${pkgname}.com/"
license=('GPL3')
makedepends=('autoconf')
source=("http://www.${pkgname}.com/source/${pkgname}-${pkgver}.tar.gz")
http://www.leptonica.com/source/leptonica-1.72.tar.gz
sha512sums=('8cb7acade68fbd9239dee4c24c5f35fd4cbb4db9e36fbf596478bd1e4635e45034664a16cec21c084091fbad64b4b6e78a4cb43fda8d0c0fc32f55a8cbf110d2')

build() {
        cd "$pkgname-$pkgver"
        ./configure --prefix=/usr
        make
}

# Uncomment next lines to enable make check step
# check() {
#         cd "$pkgname-$pkgver"
#         make -j1 check
# }

package() {
        cd "$pkgname-$pkgver"
        make DESTDIR="$pkgdir/" install
}
