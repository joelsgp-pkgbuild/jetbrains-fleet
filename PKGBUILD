# Maintainer: jmcb <joelsgp@protonmail.com>
pkgname=jetbrains-fleet
_name=Fleet
pkgver=1.9.231
pkgrel=1
pkgdesc="The next-generation IDE by JetBrains"
arch=('x86_64')
url="https://www.jetbrains.com/fleet/"
license=('custom')
# todo: deps and settings
depends=()
makedepends=()
checkdepends=()
optdepends=()
provides=()
conflicts=()
source=("https://download-cdn.jetbrains.com/fleet/installers/linux_x64/${_name}-${pkgver}.tar.gz"
        "${pkgname}.desktop")
sha256sums=('0e233e000651667b25072d0892ac69ebb31da93b7169dfdf2016efa68a2b094e'
            'f925258e3aceb9642c1d4f2e0a96b848b2f21f2ca9cda94848e732cdf0791870')


package() {
  local _dest="${pkgdir}/opt/${pkgname}"
  local _share="${pkgdir}/usr/share"

  # todo: license file in standard location
  install -Dm644 "${pkgname}.desktop" "${_share}/applications/${pkgname}.desktop"

  cd "${_name}"
  install -Dm644 "lib/${_name}.png" "${_share}/pixmaps/${pkgname}.png"

  install -d "${_dest}"
  cp -r -t "${_dest}" backend bin lib license
}
