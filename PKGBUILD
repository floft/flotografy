# Contributor: Garrett <http://floft.net/contact>
pkgname=flotografy
pkgver=0.1
pkgrel=1
pkgdesc="A simple script to generate some tone-mapped images using pfstmo."
arch=('any')
url="http://floft.net/wiki/Scripts/Flotografy"
license=('GPL')
#Depends: nmap is for flotografy_farm
depends=('enblend-enfuse' 'imagemagick' 'perl-exiftool' 'pfstmo' 'pfstools' 'gimp-ufraw' 'nmap')
backup=('etc/rc.d/flotografy_farm')
makedepends=('curl')

build() {
  curl https://raw.github.com/Floft/Flotografy/raw/master/$pkgname -so $srcdir/$pkgname
  curl https://raw.github.com/Floft/Flotografy/raw/master/${pkgname}_dirs -so $srcdir/${pkgname}_dirs
  curl https://raw.github.com/Floft/Flotografy/raw/master/${pkgname}_farm -so $srcdir/${pkgname}_farm
  curl https://raw.github.com/Floft/Flotografy/raw/master/${pkgname}_farm.daemon -so $srcdir/${pkgname}_farm.daemon
  install -Dm755 $srcdir/$pkgname $pkgdir/usr/bin/$pkgname
  install -Dm755 $srcdir/${pkgname}_dirs $pkgdir/usr/bin/${pkgname}_dirs
  install -Dm755 $srcdir/${pkgname}_farm $pkgdir/usr/bin/${pkgname}_farm
  install -Dm755 $srcdir/${pkgname}_farm.daemon $pkgdir/etc/rc.d/${pkgname}_farm
}
