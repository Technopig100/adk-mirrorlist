# Maintainer: Jacob Durant <technopig@hotmail.com>

pkgname=adk-mirrorlist-git
pkgver=23.02
pkgrel=01
pkgdesc="ADK-Linux mirror list for use by pacman"
arch=('any')
url="https://github.com/Technopig100/adk-mirrorlist.git"
license=('GPL')
backup=(etc/pacman.d/adk-mirrorlist)
source=(adklinux-mirrorlist)

# NOTE on building this package:
# * Update the checksums, update pkgver
# * Build the package

pkgver() {
  date +%y.%m
}

updatelist() {
  rm -f adklinux-mirrorlist
  curl -o adklinux-mirrorlist https://raw.githubusercontent.com/Technopig100/adk-mirrorlist/main/adklinux-mirrorlist
}

package() {
  mkdir -p "$pkgdir/etc/pacman.d"
  install -m644 "$srcdir/adklinux-mirrorlist" "$pkgdir/etc/pacman.d/"
}

md5sums=('2d947a0f1ce0dc859f19412e455fd9f5')
sha256sums=('f54e9233c61f17d9914cb8ce4ac1b43101b71c847b6908f12e5e1076f16c5ca3')
