
# Maintainer: Mequam <blue9ja@gmail.com>
pkgname="samgob"
pkgver=1.2.0
pkgrel=0
pkgdesc="a dice rolling application for all the samon goblins of the world"
arch=("x86_64")
url="https://github.com/Mequam/samgob"
makedepends=()
source=("https://raw.githubusercontent.com/Mequam/samgob_cli/master/main.py")
md5sums=("ba19f939f3cf365abc2f2d240ad1089f")
#license=('UNKOWIN')
#groups=()
depends=(python)
#checkdepends=()
#optdepends=()
#provides=()
#conflicts=()
#replaces=()
#backup=()
#options=()
#install=
#changelog=

#noextract=()
#validpgpkeys=()

prepare() {
	cd "${srcdir}"
	if [ ! -d "samgob" ]; then
	   pip install samgob --target .
	else
		echo "[prepare] source already downloaded!"
	fi
}

build() {
   mv ../main.py main.py
}

package() {
	mkdir -p "${pkgdir}/opt/samgob"
	mkdir -p "${pkgdir}/usr/bin"
	cp -r "${srcdir}"/* "${pkgdir}/opt/samgob"
	ln -s "${pkgdir}/opt/samgob/main.py" "${pkgdir}/usr/bin/samgob"
	chmod +x "${pkgdir}/usr/bin/samgob"
}

