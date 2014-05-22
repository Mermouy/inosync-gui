# Maintainer: MerMouY <mermouy@openmailbox.com>

pkgname=inosync-gui-git
pkgver=0.1
pkgrel=1
pkgdesc='inosync-gui NOT USABLE'
arch=(any)
url='https://blog.youm.org/projets/inosync-gui'
license=('GPL')
depends=('yad')
makedepends=('git')
groups=('kf5')
conflicts=(inosync-gui)
provides=(inosync-gui)
source=('https://github.com/Mermouy/inosync-gui')
md5sums=('SKIP')
pkgdir=/usr/local
pkgver() {
  cd inosync-gui
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

prepare() {
  mkdir -p build
}

build() {
  cd build
  ./inosync-gui --update
}

package() {
  cd build
  make DESTDIR="${pkgdir}" install
}
