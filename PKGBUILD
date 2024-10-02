pkgname='python-kiyoi-image-viewer'
_module='kiyoi-image-viewer'
_src_folder='kiyoi_image_viewer-0.1.1'
pkgver='0.1.1'
pkgrel=1
pkgdesc="Python image viewer based on Pyside6 and Pillow"
url="https://pypi.org/project/kiyoi-image-viewer/"
depends=('python' 'pyside6' 'python-pyperclip' 'python-pillow' 'xsel')
makedepends=('python-build' 'python-installer' 'python-wheel')
license=('custom:ISC License (ISCL)')
arch=('any')
source=("https://files.pythonhosted.org/packages/b3/0e/0bff51fcab5562021d9faf385ee535bd0b7ff60daf78ce15e3bd16d030e2/kiyoi_image_viewer-0.1.1.tar.gz")
sha256sums=('b63129e97c44daf62976dff7ba9ca858961648b498b3bc945df291f53b513c84')

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
