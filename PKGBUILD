# Maintainer: Felix Yan <felixonmars@gmail.com>
# Contributor: poplarch <poplarch@gmail.com>

pkgname=fcitx-libpinyin
pkgver=0.2.1
pkgrel=1
pkgdesc="Libpinyin Wrapper for Fcitx."
arch=('i686' 'x86_64')
url="https://github.com/fcitx/fcitx-libpinyin"
license=('GPL')
depends=('fcitx>=4.2.0' 'libpinyin>=0.3.0')
makedepends=('cmake' 'intltool')
provides=('fcitx-libpinyin')
source=("http://fcitx.googlecode.com/files/${pkgname}-${pkgver}.tar.xz")

build() {
  cd "$srcdir"/${pkgname}-${pkgver}

  rm -rf build
  mkdir build
  cd build

  msg "Starting make..."

  cmake -DCMAKE_INSTALL_PREFIX=/usr -DCMAKE_BUILD_TYPE=Release ..
  make
}

package() {
  cd "$srcdir"/${pkgname}-${pkgver}/build
  make DESTDIR="${pkgdir}" install
}
md5sums=('9ff621f6f16ab426ff01652b1ffc06a7')
