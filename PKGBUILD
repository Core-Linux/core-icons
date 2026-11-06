# Maintainer: ArchLatam <corelinux@gmail.com>

pkgname=core-icons
pkgver=r10.344392a
pkgrel=1
pkgdesc="Core-Linux icons for ArchLatam"
arch=('any')
url="https://github.com/Core-Linux/core-icons"
license=('GPL-3.0-only')
depends=('hicolor-icon-theme')
makedepends=('git')

source=("${pkgname}::git+${url}.git")
sha256sums=('SKIP')

pkgver() {
  cd "${srcdir}/${pkgname}"
  printf 'r%s.%s' \
    "$(git rev-list --count HEAD)" \
    "$(git rev-parse --short HEAD)"
}

package() {
  install -Dm644 \
    "${srcdir}/${pkgname}/usr/share/icons/corelinux.png" \
    "${pkgdir}/usr/share/icons/corelinux.png"

  install -Dm644 \
    "${srcdir}/${pkgname}/LICENSE" \
    "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
