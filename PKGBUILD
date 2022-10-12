# Maintainer: jmcb <joelsgp@protonmail.com>
pkgname=jetbrains-fleet
_name=Fleet
pkgver=1.9.231
pkgrel=1
pkgdesc="The next-generation IDE by JetBrains"
arch=('x86_64')
url="https://www.jetbrains.com/fleet/"
license=('custom')
depends=()
makedepends=()
checkdepends=()
optdepends=()
provides=()
conflicts=()
source=("https://download-cdn.jetbrains.com/fleet/installers/linux_x64/${_name}-${pkgver}.tar.gz"
        "${pkgname}.desktop")
sha256sums=('0e233e000651667b25072d0892ac69ebb31da93b7169dfdf2016efa68a2b094e'
            '7e50bf749c1575139469b40b073e90e6aa1e28dfbc71d2c6ddc4650176aa78a1')


package() {
  local _dest="${pkgdir}/opt/${pkgname}"
  local _share="${pkgdir}/usr/share"

  install -Dm644 "${pkgname}.desktop" "${_share}/applications/${pkgname}.desktop"

  cd "${_name}"
  install -Dm644 "lib/${_name}.png" "${_share}/pixmaps/${pkgname}.png"

  install -d "${_dest}"
  cp -r -t "${_dest}" backend bin lib license
}
