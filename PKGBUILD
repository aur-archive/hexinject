# Maintainer: Guillermo Ramos <0xwille at gmail dot com>

pkgname="hexinject"
pkgver=1.5
pkgrel=1
pkgdesc="A very versatile packet injector and sniffer, that provide a command-line framework for raw network access"
arch=('i686' 'x86_64')
url="http://hexinject.sourceforge.net"
license=('BSD')
depends=('libpcap')
source=("http://sourceforge.net/projects/${pkgname}/files/${pkgname}-${pkgver}/${pkgname}-${pkgver}.tar.gz/download"
		"COPYING")
md5sums=('26fbb396bed9c64de653e35ae78b6956'
		'78ee1a3580a696ba78e8903a76c1955a')
sha256sums=('329f0686069988ac0dae4a00082b205ac9669bc8e202d4b112c600bcbc198ce9'
		'd6c66830395da3461a5d599d3cc814f7697c25fac2e1b1ba6d1a64a86d9bddb8')

build() {
	cd "$srcdir/$pkgname"

	msg "Building..."
	make

	msg "Installing..."
	install -D -m755 $srcdir/$pkgname/hexinject $pkgdir/bin/hexinject
	install -D -m755 $srcdir/$pkgname/prettypacket $pkgdir/bin/prettypacket
	install -D -m755 $srcdir/$pkgname/hex2raw $pkgdir/bin/hex2raw
	install -D -m755 $srcdir/COPYING $pkgdir/usr/share/licenses/$pkgname/COPYING
}
