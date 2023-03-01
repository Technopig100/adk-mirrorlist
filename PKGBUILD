# Maintainer: Jacob Durant <technopig@hotmail.com>

pkgname=adk-mirrorlist
pkgver=230226
pkgrel=1
pkgdesc="ADK-Linux mirror list for use by pacman"
arch=('any')
url="https://github.com/Technopig100/adk-mirrorlist.git"
license=('GPL')
backup=(etc/pacman.d/adk-mirrorlist)
source=(adk-mirrorlist)

# NOTE on building this package:
# * Update the checksums, update pkgver
# * Build the package

pkgver() {
  date +%y.%m
}

package() {
  mkdir -p "$pkgdir/etc/pacman.d"
  install -m644 "$srcdir/adk-mirrorlist" "$pkgdir/etc/pacman.d/"
}

md5sums=('8509a072494866a4d5092ff3350cdaf6')
sha256sums=('aaa43f97adf0e0a5bbf8f2668237aa1d7aa35fd6e99d639602aabde09756c392')
