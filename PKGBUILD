# Contributor: Tilman Bartsch <tba@timaba.de>

pkgname=spicebird-bin-de
_pkgname=spicebird-beta
pkgver=0.7de
_pkgver=0.7
pkgrel=1
pkgdesc="Mozilla-based Personal Information Manager - Precompiled i686 binary"
arch=('i686')
url="http://www.spicebird.org/"
license=('GPL' 'LGPL' 'MPL')
depends=('libgnomecanvas' 'libxt' 'nss' 'dbus-glib' 'popt')
provides=('spicebird')
source=(http://files.spicebird.org/pub/spicebird.org/spicebird/releases/$_pkgver/linux-i686/de/$_pkgname-$_pkgver.de.linux-i686.tar.bz2 spicebird-bin-de.desktop)
md5sums=('f00f7e8c1cc6389be8b522a6722202a4' '0f9188f8c6d4d177d65bd0507da183d0')

build() {
  
  cd $startdir/src/$_pkgname
 
  #Libs provided by nspr
  rm libnspr4.so libplc4.so libplds4.so
  
  mkdir $startdir/pkg/opt/$pkgname/ -p
  cp $startdir/src/$_pkgname/* $startdir/pkg/opt/$pkgname/ -r
  
  mkdir $startdir/pkg/usr/share/{applications,pixmaps} -p
  install -m644 $startdir/src/$_pkgname/icons/mozicon50.xpm  $startdir/pkg/usr/share/pixmaps/spicebird.xpm
  install -m644 $startdir/src/spicebird-bin-de.desktop $startdir/pkg/usr/share/applications/
}

