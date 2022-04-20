# Maintainer: Jose C.

pkgname=jetbrains-clion
pkgver='2022.1'
pkgrel=1
pkgdesc='A cross-platform IDE for C and C++'
arch=('x86_64')
options=('!strip' 'staticlibs')
url='https://www.jetbrains.com/clion/'
license=('Commercial')
optdepends=('cmake' 'make')
provides=('clion')
conflicts=('clion')

_filename="CLion-${pkgver}.tar.gz"
_filextract="clion-$pkgver"


source=("https://download.jetbrains.com/cpp/${_filename}"
	"${pkgname}.desktop")

sha256sums=( 'a8ad8db6362d60a5ce60a7552110887dbd12e8420c839c368b55808b68dea38b'
	'3039173e17b1287843c304600995215e4a57faac0cc13fb293709b4c9a85e8f1')

package() {
	#Create directories with permission rwxr-xr-x
	install -m755 -d "${pkgdir}/usr/share" "${pkgdir}/usr/bin" "${pkgdir}/usr/share/applications"

	#Copy files to pkg destination
	cp -r "${srcdir}/${_filextract}" "${pkgdir}/usr/share/${pkgname}"
  chown -R root:root "${pkgdir}/usr/share/${pkgname}"

	ln -s "/usr/share/${pkgname}/bin/clion.sh" "${pkgdir}/usr/bin/clion"
  install -m644 "${srcdir}/${pkgname}.desktop" "${pkgdir}/usr/share/applications"
}
