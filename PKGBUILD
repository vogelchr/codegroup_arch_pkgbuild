# Codegroup by John Walker (Fourmilab)
# Christian Vogel <vogelchr@vogel.cx>

pkgname=codegroup
pkgver=1.0
pkgrel=1
pkgdesc="Encodes and decodes arbitrary binary data in five-letter code groups, just like spies use"
arch=('i686' 'x86_64')
url="https://www.fourmilab.ch/codegroup/"
license=('unknown')
depends=('ncurses')
source=("codegroup.zip")
sha1sums=('ea6d4e86f34989d7cddb6ce18e8eaa7545c41de4')

build() {
  # the zip unpacks right into srcdir, doesn't create
  # sub directories
  cd "$srcdir"
  make
  gzip -9k "$pkgname.1"
}

package() {
 cd "$srcdir"
 install -Dm755 $pkgname "$pkgdir/usr/bin/$pkgname"
 install -Dm644 $pkgname.1.gz "$pkgdir/usr/share/man/man1/$pkgname.1.gz"
} 
