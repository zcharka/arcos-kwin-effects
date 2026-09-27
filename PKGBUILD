pkgname=arcos-kwin-effects
pkgver=1.0.0
pkgrel=1
pkgdesc='ArcOS integration for KWin Glass and Rounded Corners effects'
arch=('any')
license=('GPL-3.0-only')
depends=(
    'kwin'
    'kwin-effects-glass-git'
    'kwin-effect-rounded-corners-git'
    'git'
    'cmake'
    'gcc'
    'make'
)

package() {
    cd "${srcdir}"

    find usr -type f | while IFS= read -r _file; do
        install -Dm755 "${_file}" "${pkgdir}/${_file}"
    done

    find etc -type f | while IFS= read -r _file; do
        install -Dm644 "${_file}" "${pkgdir}/${_file}"
    done
}
