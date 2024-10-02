pkgname='python-kiyoi-image-viewer'
_module='kiyoi-image-viewer'
_src_folder='kiyoi_image_viewer-0.1.2'
pkgver='0.1.2'
pkgrel=1
pkgdesc="Python image viewer based on Pyside6 and Pillow"
url="https://pypi.org/project/kiyoi-image-viewer/"
depends=('python' 'pyside6' 'python-pyperclip' 'python-pillow' 'xsel')
makedepends=('python-build' 'python-installer' 'python-wheel')
license=('custom:ISC License (ISCL)')
arch=('any')
source=("https://files.pythonhosted.org/packages/2d/65/5fca8f8e8b2fca9fee6921bf491f63c0e1eade0ec3fff3c25c078c6be382/kiyoi_image_viewer-0.1.2.tar.gz")
sha256sums=('5379bfde3c12b62fa425d068bb6f464dfce736e135e825da9568836ab22370e0')

build() {
    cd "${srcdir}/${_src_folder}"
    python -m build --wheel --no-isolation
}

package() {
    cd "${srcdir}/${_src_folder}"
    python -m installer --destdir="${pkgdir}" dist/*.whl
    install -Dm644 "${srcdir}/${_src_folder}/LICENSE.txt" "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE.txt"
    install -Dm644 "${srcdir}/${_src_folder}/kiyoi_image_viewer.desktop" "${pkgdir}/usr/share/applications/kiyoi_image_viewer.desktop"
    install -Dm644 "${srcdir}/${_src_folder}/src/kiyoi_image_viewer/resources/kiyoi.svg" "${pkgdir}/usr/share/icons/hicolor/scalable/apps/kiyoiiv.svg"
    install -Dm644 "${srcdir}/${_src_folder}/src/kiyoi_image_viewer/resources/kiyoi384.png" "${pkgdir}/usr/share/icons/hicolor/384x384/apps/kiyoiiv.png"
    install -Dm644 "${srcdir}/${_src_folder}/src/kiyoi_image_viewer/resources/kiyoi256.png" "${pkgdir}/usr/share/icons/hicolor/256x256/apps/kiyoiiv.png"
    install -Dm644 "${srcdir}/${_src_folder}/src/kiyoi_image_viewer/resources/kiyoi192.png" "${pkgdir}/usr/share/icons/hicolor/192x192/apps/kiyoiiv.png"
    install -Dm644 "${srcdir}/${_src_folder}/src/kiyoi_image_viewer/resources/kiyoi128.png" "${pkgdir}/usr/share/icons/hicolor/128x128/apps/kiyoiiv.png"
    install -Dm644 "${srcdir}/${_src_folder}/src/kiyoi_image_viewer/resources/kiyoi64.png" "${pkgdir}/usr/share/icons/hicolor/64x64/apps/kiyoiiv.png"
    install -Dm644 "${srcdir}/${_src_folder}/src/kiyoi_image_viewer/resources/kiyoi48.png" "${pkgdir}/usr/share/icons/hicolor/48x48/apps/kiyoiiv.png"
    install -Dm644 "${srcdir}/${_src_folder}/src/kiyoi_image_viewer/resources/kiyoi32.png" "${pkgdir}/usr/share/icons/hicolor/32x32/apps/kiyoiiv.png"
    install -Dm644 "${srcdir}/${_src_folder}/src/kiyoi_image_viewer/resources/kiyoi24.png" "${pkgdir}/usr/share/icons/hicolor/24x24/apps/kiyoiiv.png"
    install -Dm644 "${srcdir}/${_src_folder}/src/kiyoi_image_viewer/resources/kiyoi22.png" "${pkgdir}/usr/share/icons/hicolor/22x22/apps/kiyoiiv.png"
    install -Dm644 "${srcdir}/${_src_folder}/src/kiyoi_image_viewer/resources/kiyoi16.png" "${pkgdir}/usr/share/icons/hicolor/16x16/apps/kiyoiiv.png"
}
