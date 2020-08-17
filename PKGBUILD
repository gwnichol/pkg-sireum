pkgname=sireum-ive
pkgver=v3
pkgrel=1
pkgdesc="Sireim IVE"
arch=("any")

SIREUM_HOME="/opt/${pkgname}/Sireum"

source=("$pkgname-$pkgver.zip::http://bit.ly/sv3ivel" "sireum-ive.desktop")
noextract=("$pkgname-$pkgver.zip" "sireum-ive.desktop")
md5sums=('SKIP' 'SKIP')

license=('custom')

package() {
	install -d -m755 "${pkgdir}/opt/${pkgname}"
	unzip "${pkgname}-${pkgver}.zip" -d "${pkgdir}/opt/${pkgname}"

	install -d -m755 "${pkgdir}/usr/bin/"
	ln -s "$SIREUM_HOME/idea" "${pkgdir}/usr/bin/sireum-idea"
	ln -s "$SIREUM_HOME/sireum" "${pkgdir}/usr/bin/sireum"

	install -d -m755 "$pkgdir/usr/share/applications"
	install -m644 "${srcdir}/sireum-ive.desktop" "${pkgdir}/usr/share/applications/"
}
