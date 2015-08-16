# Maintainer: Antonio Rojas
# Contributor: Andrea Scarpino <andrea@archlinux.org>
# Contributor: Balló György <ballogyor+arch at gmail dot com>

pkgname=libaccounts-qt5
pkgver=1.13
pkgrel=1
_gitrev=2a9cc22ff7b0
arch=('i686' 'x86_64')
pkgdesc="Qt-based client library for accessing the online accounts database"
url="http://code.google.com/p/accounts-sso/"
license=('LGPL')
depends=('qt5-base' 'libaccounts-glib')
makedepends=('doxygen')
source=("http://libaccounts-qt.accounts-sso.googlecode.com/archive/$pkgver.tar.gz")
sha1sums=('SKIP') # changes with every download

build() {
  cd libaccounts-qt.accounts-sso-$_gitrev
  qmake-qt5 PREFIX=/usr LIBDIR=/usr/lib
  make
}

package() {
  cd libaccounts-qt.accounts-sso-$_gitrev
  make INSTALL_ROOT="$pkgdir" install_subtargets
}
