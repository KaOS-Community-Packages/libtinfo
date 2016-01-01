pkgname=libtinfo
pkgver=6
pkgrel=1
pkgdesc="symlink to ncurses for use in cuda and other packages"
arch=('x86_64')
url="http://www.gnu.org/software/ncurses/"
license=('unknown')
depends=('ncurses>=6.0')
_ncurses="$(pacman -Q ncurses | awk '{sub(/-[0-9]+/, "", $2); print $2}')"

package() {
  install -d "$pkgdir"/usr/lib
  ln -s /usr/lib/libncursesw.so."$_ncurses" "$pkgdir"/usr/lib/libtinfo.so."$pkgver"
  ln -s /usr/lib/libtinfo.so."$pkgver" "$pkgdir"/usr/lib/libtinfo.so
  ln -s /usr/lib/libtinfo.so."$pkgver" "$pkgdir"/usr/lib/libtinfo.so.5
} 
