# Maintainer:
# Contributor:
# Contributor: Sergej Pupykin <pupykin.s+arch@gmail.com>
# Contributor: Jonathan Liu <net147@gmail.com>

pkgname='python2-ipaddr'
pkgver=2.2.0
pkgrel=1
pkgdesc="An IPv4/IPv6 manipulation library in Python"
arch=('any')
url="http://code.google.com/p/ipaddr-py/"
license=('APACHE')
depends=('python2')
makedepends=('python2-setuptools')
source=("https://pypi.python.org/packages/source/i/ipaddr/ipaddr-${pkgver}.tar.gz")
sha512sums=('5adb117c44e6e5dbdb9e96543aa7a34f35b4a4ec9baa163a25448058c34091bf4019d24f0250928291e4d4bc97dcdf75865daef739e2d94f98cc584e6e6c50dd')

prepare() {
  cd ipaddr-$pkgver
  sed -e 's|/usr/bin/python|/usr/bin/python2|' -i ipaddr.py
}

check() {
  cd ipaddr-$pkgver
  python2 ipaddr_test.py
}

package() {
  cd ipaddr-$pkgver
  python2 setup.py install --root="${pkgdir}" -O1
}
