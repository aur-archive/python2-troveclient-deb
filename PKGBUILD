# Maintainer: James Bulmer <nekinie@gmail.com>

pkgname="python2-troveclient-deb"
pkgver=1.0.3
pkgrel=2
pkgdesc="Client library for Openstack"
arch=("i686" "x86_64")
url="http://docs.openstack.org/developer/trove/"
license=("Apache")

depends=(
  "python2"
  "python2-pbr"
  "python2-prettytable"
  "python2-requests"
  "python2-simplejson"
  "python2-babel"
  "python2-six"
)

makedepends=("python2-setuptools")
conflicts=("python2-troveclient" "python2-troveclient-git")
source=("http://archive.ubuntu.com/ubuntu/pool/main/p/python-troveclient/python-troveclient_${pkgver}.orig.tar.gz")
md5sums=("33ded699896801e66ed8a7a1b13faff5")

build() {
  cd "${srcdir}/python-troveclient-${pkgver}/"
  python2 setup.py build
}

package() {
  cd "${srcdir}/python-troveclient-${pkgver}/"
  python2 setup.py install --root="${pkgdir}/" --optimize=1
}