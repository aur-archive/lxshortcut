# Contributor: zoulnix <http://goo.gl/HQaP>
# Contributor: n6W588kJ2d
pkgname=lxshortcut
pkgver=0.1.2
pkgrel=1
pkgdesc="Small program used to edit application shortcuts (part of LXDE)."
arch=('i686' 'x86_64')
url="http://lxde.org/"
license=('GPL')
depends=('gtk2')
makedepends=('autoconf' 'automake' 'gcc' 'intltool' 'make' 'pkg-config')
options=('!libtool')
groups=('lxde')
source=(http://downloads.sourceforge.net/lxde/${pkgname}-${pkgver}.tar.gz) 
md5sums=( '72f0dfafa8098be853beae6e33b5e13b' )

build() {
  cd ${srcdir}/${pkgname}-${pkgver}


  ./configure --prefix=/usr \
	      --sysconfdir=/etc \
	      --localstatedir=/var

  make
}

package() {
  cd ${srcdir}/${pkgname}-${pkgver}

  make DESTDIR=${pkgdir} install
}
