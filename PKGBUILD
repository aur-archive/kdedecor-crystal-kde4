# Maintainer: b00rt00s ( bomby dot zrzuc at gmail dot com )
# Contributor: Carl Mueller  arch at carlm e4ward com

pkgname=kdedecor-crystal-kde4
pkgver=2.2.1
pkgrel=1
arch=(i686 x86_64)
pkgdesc="Crystal decoration theme for KDE4.x"
url="http://www.kde-look.org/content/show.php?content=75140"
license="GPL"
depends=('kdebase-runtime' 'kdebase-workspace')
makedepends=('cmake' 'automoc4')
source=(http://kde-look.org/CONTENT/content-files/75140-crystal-${pkgver}.tar.bz2)
md5sums=('02e2a25ce02a974dc8c23fbdd40a2705')

build() {
  cd ${srcdir}/crystal-${pkgver}
  cmake -DCMAKE_INSTALL_PREFIX=`kde4-config --prefix` .
  make -j1 || return 1
  make DESTDIR=${pkgdir} install
}
