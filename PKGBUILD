# $Id: PKGBUILD 82330 2013-01-15 11:35:00Z allan $
# Maintainer: Mateusz Herych <heniekk@gmail.com>

pkgname=gmerlin-avdecoder
pkgver=1.2.0
pkgrel=2
pkgdesc="Media decoding library"
arch=('i686' 'x86_64')
url="http://gmerlin.sourceforge.net/avdec_frame.html"
license=('GPL')
depends=('gmerlin' 'openjpeg' 'flac' 'smbclient' 'libmad' 'libmpcdec' 'speex'
         'libdca' 'libmpeg2' 'a52dec')
source=(http://downloads.sourceforge.net/sourceforge/gmerlin/gmerlin-avdecoder-$pkgver.tar.gz)
md5sums=('37b19266b098d9d05bb05ebef138ffbd')

build() {
  cd "$srcdir/$pkgname-$pkgver"
  rm -f cpuinfo.sh
  ./configure --prefix=/usr --without-doxygen
  make
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  make DESTDIR="$pkgdir" install
}
