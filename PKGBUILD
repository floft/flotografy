# Contributor: Garrett <http://floft.net/contact>
pkgname=flotografy
pkgver=0.1
pkgrel=1
pkgdesc="A simple script to generate some tone-mapped images using pfstmo."
arch=('any')
url="http://floft.net/wiki/Scripts/Flotografy"
license=('GPL')
depends=('enblend-enfuse' 'imagemagick' 'perl-exiftool' 'pfstmo' 'pfstools' 'gimp-ufraw')
makedepends=('curl')

build() {
  curl https://github.com/Floft/Flotografy/raw/master/$pkgname -so $srcdir/$pkgname
  curl https://github.com/Floft/Flotografy/raw/master/${pkgname}_dirs -so $srcdir/${pkgname}_dirs
  install -Dm755 $srcdir/$pkgname $pkgdir/usr/bin/$pkgname
  install -Dm755 $srcdir/${pkgname}_dirs $pkgdir/usr/bin/${pkgname}_dirs
}
