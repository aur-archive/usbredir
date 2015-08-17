# Maintainer: Stefano Facchini <stefano.facchini@gmail.com>
pkgname=usbredir
pkgver=0.6
pkgrel=3
pkgdesc="USB traffic redirection protocol"
arch=('i686' 'x86_64')
url="http://spice-space.org/page/UsbRedir"
license=('GPL2' 'LGPL2.1')
depends=('libusb')
options=(!libtool)
source=(http://spice-space.org/download/usbredir/$pkgname-$pkgver.tar.bz2)
sha256sums=('028184960044ea4124030000b3c55a35c3238835116e3a0fbcaff449df2c8edf')

build() {
  cd "$srcdir/$pkgname-$pkgver"
  ./configure --prefix=/usr --sbindir=/usr/bin

  make
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  make DESTDIR="$pkgdir/" install
}

# vim:set ts=2 sw=2 et:
