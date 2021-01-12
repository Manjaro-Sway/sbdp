# # Maintainer: Jonas Strassel (info@jonas-strassel.de)

pkgname=sbdp
pkgver=1.0.0
pkgrel=2
pkgdesc='SwayBindsymDocsParser (sbdp) is a small parser for keybinding hints in a compact form suitable for tiling window environments.'
url="https://github.com/boredland/sbdp"
arch=('any')
license=('MIT')
depends=('nodejs>=12.0.0')
provides=('sbdp')
makedepends=(
    'npm>=5.0.0'
)
source=("$pkgname-$pkgver.tar.gz::https://github.com/boredland/${pkgname}/archive/${pkgver}.tar.gz")
md5sums=("SKIP")

build() {
    cd "${srcdir}/${pkgname}-${pkgver}"
    npm i
    npm run build
}

package() {
    install -D -m 0755 "${srcdir}/${pkgname}-${pkgver}/dist/index.js" "${pkgdir}/usr/bin/sbdp"
}