# Maintainer:
# Contributor: Sven-Hendrik Haase <sh@lutzhaase.com>
# Contributor: Lauri Niskanen <ape@ape3000.com>
# Contributor: Ray Rashif <schiv@archlinux.org>

pkgname=celt-0.7
_realname=celt
pkgver=0.7.1
pkgrel=4
pkgdesc='Low-latency audio communication codec'
arch=('i686' 'x86_64')
url='http://www.celt-codec.org'
license=('BSD')
depends=('libogg')
#provides=('celt=$pkgver')
conflicts=('celt')
options=('!libtool')
source=("http://downloads.xiph.org/releases/celt/$_realname-$pkgver.tar.gz")
md5sums=('c7f6b8346e132b1a48dae0eff77ea9f0')

build() {
  cd "$srcdir/$_realname-$pkgver"

  ./configure --prefix=/usr
  make
}

package() {
	cd "$srcdir/$_realname-$pkgver"

  make DESTDIR="$pkgdir/" install
  install -Dm644 COPYING \
    "$pkgdir/usr/share/licenses/$pkgname/BSD"
}

# vim:set ts=2 sw=2 et:
