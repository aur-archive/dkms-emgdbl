# Maintainer: Gustavo Alvarez <sl1pkn07@gmail.com>

pkgname=dkms-emgdbl
_modname=emgdbl
pkgver=0.1beta7
_pkgver=0.1alpha2
pkgrel=5
pkgdesc="Intel EMGD backlight driver in DKMS format."
arch=('i686')
url="http://edc.intel.com/Software/Downloads/EMGD/"
license=('custom')
depends=('dkms-emgd' 'xf86-video-emgd' 'dkms')
provides=('emgdbl')
install="${pkgname}".install
source=(https://launchpad.net/~gma500/+archive/emgd110/+files/"${_modname}"_"${pkgver}".tar.gz
        "${pkgname}".install)
md5sums=('3f400b14c5e9e0ef222878fd63bfe7b7'
         '65ed00ae07f3c325a3adc76d12a68798')

build() {
    cd "${srcdir}"
}

package() {
    mkdir -p "${pkgdir}"/usr/src/"${_modname}"-"${_pkgver}"
    cp -R "${srcdir}"/"${_modname}"/* "${pkgdir}"/usr/src/"${_modname}"-"${_pkgver}"
    rm -fr "${pkgdir}"/usr/src/"${_modname}"-"${_pkgver}"/debian
}
