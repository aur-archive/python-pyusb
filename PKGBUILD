# Maintainer: Jonathan Kotta <jpkotta AT gmail DOT com>

pkgname=python-pyusb
pkgver=1.0.0b2
pkgrel=2
pkgdesc="A pure Python module which provides USB access."
arch=('any')
url="https://github.com/walac/pyusb"
license=('custom')
depends=('python' 'libusb-compat')
makedepends=('python-distribute')
provides=($pkgname)
conflicts=($pkgname-git)
source=("https://github.com/walac/pyusb/archive/${pkgver}.tar.gz")
md5sums=('bc12e83ff3ef1045d4306d13a9955fc1')

build() {
	cd $srcdir/pyusb-$pkgver
	python setup.py build
}

package() {
	cd $srcdir/pyusb-$pkgver
	python setup.py install -f --root="$pkgdir"
	install -Dm644 LICENSE "$pkgdir"/usr/share/licenses/$pkgname/LICENSE
}
