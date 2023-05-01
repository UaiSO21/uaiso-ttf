# Maintainer: Barnabé di Kartola <barnabedikartola@gmail.com>

pkgname=uaiso-ttf
pkgver=$(date +%y.%m.%d)
pkgrel=$(date +%H%M)
pkgdesc="Package Base ttf UaiSO21"
arch=('any')
url="https://github.com/UaiSO21/$pkgname"
license=('GPL3')
depends=(ttf-ms-fonts ttf-roboto noto-fonts-emoji)
provides=("$pkgname")
# conflicts=('')
source=("git+${url}.git")
md5sums=('SKIP')
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
