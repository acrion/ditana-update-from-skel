# Maintainer: Stefan Zipproth <s.zipproth@ditana.org>

pkgname=ditana-update-from-skel
pkgver=1.06
pkgrel=1
pkgdesc="Ditana script to copy updated files from /etc/skel to the current user’s home directory"
arch=(any)
url="https://ditana.org"
license=('AGPL-3.0-or-later')
conflicts=()
depends=(diffutils)
makedepends=()
source=(
'update-from-skel'
'update-from-skel.1'
)
sha256sums=(
'SKIP'
'SKIP'
)

package() {
	install -D -m755 $srcdir/update-from-skel $pkgdir/usr/bin/update-from-skel
    install -Dm644 "update-from-skel.1" "$pkgdir/usr/share/man/man1/update-from-skel.1"
}
