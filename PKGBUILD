pkgname=leptonica
pkgver=1.79.0
pkgrel=1
pkgdesc="Software that is broadly useful for image processing and image analysis applications"
arch=('x86_64')
url="http://www.leptonica.com/"
license=('custom')
depends=('giflib' 'libjpeg-turbo' 'libpng' 'libtiff' 'zlib' 'libwebp')
source=("$pkgname-$pkgver.tar.gz::https://github.com/DanBloomberg/leptonica/archive/$pkgver.tar.gz")
sha256sums=('bf9716f91a4844c2682a07ef21eaf68b6f1077af1f63f27c438394fd66218e17')

prepare() {
  cd "$srcdir"/leptonica-${pkgver}
  ./autogen.sh
}

build() {
  cd "$srcdir"/leptonica-${pkgver}
  ./configure --prefix=/usr
  make
}

package() {
  cd "$srcdir"/leptonica-${pkgver}
  make DESTDIR="$pkgdir" install
  install -D leptonica-license.txt "$pkgdir"/usr/share/licenses/leptonica/leptonica-license.txt
}
