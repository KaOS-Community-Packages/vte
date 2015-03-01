pkgname='vte'
pkgver=3.9.90
pkgrel=1
pkgdesc="Virtual Terminal Emulator widget for use with GTK3"
arch=('x86_64')
url=("http://ftp.gnome.org/pub/GNOME/sources/vte/0.39/")
license=('LGPL')
makedepends=('vala' 'glibc' 'gtk3' 'intltool>=0.35' 'python2')
provides=('vte' 'vte3')
source=("$pkgname::http://ftp.gnome.org/pub/GNOME/sources/vte/0.39/vte-0.39.90.tar.xz")

depends=('vala>=0.26.2-1')

sha256sums=("9d127e8dc9ca8267fe65f280bf3afb17d68ef154163f84b3bb2fc79e73abbc97")

build() {
	
	cd $srcdir/vte-0.39.90
	./configure --prefix=/usr
	make 
}

package() {
	pwd
	cd $srcdir/vte-0.39.90
	pwd
	make DESTDIR="$pkgdir/" install
}
