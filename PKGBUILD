pkgname='vte'
pkgver=3.9.90
pkgrel=1
pkgdesc="Virtual Terminal Emulator widget for use with GTK3"
arch=('x86_64')
url=("http://ftp.gnome.org/pub/GNOME/sources/$pkgname/0.39/")
license=('LGPL')
depends=('vala')
makedepends=('glibc' 'gtk3' 'intltool' 'python2')
source=("$pkgname::http://ftp.gnome.org/pub/GNOME/sources/$pkgname/0.39/$pkgname-0.39.90.tar.xz")
sha256sums=("9d127e8dc9ca8267fe65f280bf3afb17d68ef154163f84b3bb2fc79e73abbc97")

build() {
	cd $srcdir/$pkgname-0.39.90
	./configure --prefix=/usr
	make 
}

package() {
	cd $srcdir/$pkgname-0.39.90
	make DESTDIR="$pkgdir/" install
}
