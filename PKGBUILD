# Maintainer: Krzysztof Wloch <wloszekk [at] gmail [dot] com>
# Contributor: Dries De Smet <driesdesmet at gmail dot com>

pkgname=neap
pkgver=0.7
pkgrel=3
pkgdesc="A simple pager that runs in the notification area / systray of your panel."
arch=(any)
url="http://code.google.com/p/neap/"
license=('custom:BSD-new')
depends=('pygtk' 'python2-xlib')
install="$pkgname.install"
source=("http://neap.googlecode.com/files/$pkgname-$pkgver.tar.gz"
	"neap.desktop")

md5sums=('d3b0df1333a47551c77b80c90fc7ad89'
         'bd49e0a8c8b5e84d85401c9ab3b9c2dd')

package() {
	install -D -m 644 neap.desktop ${pkgdir}/usr/share/applications/neap.desktop

	cd ${srcdir}/$pkgname-$pkgver

	install -D -m 644 License.txt ${pkgdir}/usr/share/licenses/${pkgname}/LICENSE
	install -D -m 644 README	${pkgdir}/usr/share/${pkgname}/README
	install -D -m 644 ChangeLog 	${pkgdir}/usr/share/${pkgname}/ChangeLog
	
	sed -i 's/python/python2/g' neap
	install -D -m 755 neap ${pkgdir}/usr/bin/neap
}
