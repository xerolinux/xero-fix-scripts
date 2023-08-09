# Maintainer: DarkXero <info@techxero.com>
pkgname=xero-fix-scripts
_destname1="/"
pkgver=1.4
pkgrel=3
pkgdesc="Some Scripted Tools"
arch=('any')
url="https://github.com/XeroLinux"
license=('GPL3')
makedepends=('git')
conflicts=('xero-fix-tools-dev')
provides=("${pkgname}")
options=(!strip !emptydirs)
source=(${pkgname}::"git+${url}/${pkgname}")
sha256sums=('SKIP')
package() {
	install -dm755 ${pkgdir}${_destname1}
	cp -r ${srcdir}/${pkgname}${_destname1}/* ${pkgdir}${_destname1}
	rm "${pkgdir}${_destname1}/push.sh"
	rm "${pkgdir}${_destname1}/README.md"
	rm "${pkgdir}${_destname1}/PKGBUILD"
	rm "${pkgdir}${_destname1}/LICENSE"
}
