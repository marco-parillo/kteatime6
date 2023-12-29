pkgname=kteatime
pkgver=23.08.4
pkgrel=1
pkgdesc='A handy timer for steeping tea'
url='https://apps.kde.org/kteatime/'
arch=(x86_64)
license=(GPL LGPL FDL)
groups=(kde-applications kde-utilities)
depends=(knotifyconfig6 hicolor-icon-theme)
makedepends=(extra-cmake-modules kdoctools6)
source=(https://download.kde.org/stable/release-service/$pkgver/src/$pkgname-$pkgver.tar.xz{,.sig})
sha256sums=('5c239e83bf83f86d63132161c5e114446a3f1a641da06976d80526760b268ca4'
            'SKIP')
validpgpkeys=("SKIP")

build() {
  cmake -B build -S $pkgname-$pkgver \
    -DBUILD_TESTING=OFF
  cmake --build build
}

package() {
  DESTDIR="$pkgdir" cmake --install build
}
