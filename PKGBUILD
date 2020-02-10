pkgname=vte
pkgver=0.59.0
pkgrel=1
pkgdesc="Virtual Terminal Emulator widget for use with GTK3"
arch=('x86_64')
url="https://wiki.gnome.org/Apps/Terminal/VTE"
license=('LGPL')
depends=('glibc' 'gtk3')
makedepends=('meson' 'ninja' 'vala')
source=("http://ftp.gnome.org/pub/GNOME/sources/$pkgname/$pkgver/$pkgname-$pkgver.tar.xz")
sha256sums=("bbd54c2ef133d0883acf2a4afbf1085087b576f4046a8728209111a604de6927")

build() {
	cd $srcdir/$pkgname-$pkgver
	meson _build --prefix=/usr
	ninja -C _build
}

package() {
	cd $srcdir/$pkgname-$pkgver
	DESTDIR=$pkgdir/ ninja -C _build install
}
