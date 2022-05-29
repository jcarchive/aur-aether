# Maintainer: Jose C.

pkgname=aether
pkgver='2.0.0_dev.15'
pkgrel=1
pkgdesc="Open source, self-governing communities with auditable moderation and mod elections"
arch=(any)
license=('AGPL')
url="https://getaether.net/download/"

_progname=Aether
_fixver="${pkgver//_/-}"
_buildid='2011262249.19338c93'
source=( "https://static.getaether.net/Releases/Aether-${_fixver}/${_buildid}/linux/Aether-${_fixver}%2B${_buildid}.tar.gz")

sha256sums=('c7d50891f10e56846c1baf45cddf91d040bf26d4c254f1be8f6c50f507e228c2')

package() {
	cd "${srcdir}"

	install -d -m755 "$pkgdir/usr/share/"
	install -d -m755 "$pkgdir/usr/bin/"

	cp -a "Aether-${_fixver}+$_buildid" "$pkgdir/usr/share/$pkgname"
	ln -s "/usr/share/$pkgname/AetherP2P" "$pkgdir/usr/bin/${pkgname}"
}
