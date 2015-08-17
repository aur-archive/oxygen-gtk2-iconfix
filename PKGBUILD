# Maintainer: directrandom <directrandom at gmail dot com>
# Contributor: birdflesh <antkoul at gmail dot com>

pkgname=oxygen-gtk2-iconfix
_pkgname=oxygen-gtk2
pkgver=1.4.6
pkgrel=1
pkgdesc="Port of the default KDE widget theme (Oxygen) to GTK2, uses GTK2 icon theme."
arch=('i686' 'x86_64')
url='https://projects.kde.org/projects/playground/artwork/oxygen-gtk/'
license=('LGPL')
depends=('gtk2')
conflicts=('oxygen-gtk' 'oxygen-gtk2')
replaces=('oxygen-gtk' 'oxygen-gtk2')
makedepends=('cmake')
source=("http://download.kde.org/stable/${_pkgname}/${pkgver}/src/${_pkgname}-${pkgver}.tar.bz2")
md5sums=('493892fc36302bfe862604f667a6c04e')

build() {
  mkdir build
  cd build
  cmake ../${_pkgname}-${pkgver} \
    -DCMAKE_BUILD_TYPE=Release \
    -DCMAKE_INSTALL_PREFIX=/usr \
    -DOXYGEN_ICON_HACK=0
  make
}

package() {
  cd build
  make DESTDIR="${pkgdir}" install
} 
