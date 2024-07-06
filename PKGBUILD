pkgname=miladi-calamares-config
pkgver=20240706
pkgrel=1
pkgdesc="Calamares config for Miladi"
arch=('any')
url="https://github.com/yuki/miladi-calamares-config"
license=('GPL3')
#makedepends=('git')
provides=("${pkgname}")
options=(!strip !emptydirs)
source=("git+file://${PWD}")
sha256sums=('SKIP')

if [ -e "${pkgname}.install" ];then
    install=${pkgname}.install
fi

package() {

    InternalDir="${srcdir}/${pkgname}"

    # Copy files
    if [ -d "${InternalDir}/usr" ]; then
        cp -r "${InternalDir}/usr" "${pkgdir}/"
    fi

    if [ -d "${InternalDir}/etc" ]; then
        cp -r "${InternalDir}/etc" "${pkgdir}/"
    fi

    if [ -d "${InternalDir}/opt" ]; then
        cp -r "${InternalDir}/opt" "${pkgdir}/"
    fi
}