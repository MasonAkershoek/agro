# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# Maintainer: Mason Akershoek <masonakershoek@gmail.com>
pkgname='agro'
pkgver=0.0.1
pkgrel=1
epoch=
pkgdesc="File agregation for the command line"
arch=(x86_64)
url="https://github.com/MasonAkershoek/Agro"
license=('GPL')
depends=('git')
makedepends=('cmake' 'gcc' 'make' 'glibc' 'glib2')
#install='agro.install'
changelog=
source=(argo::git://github.com/MasonAkershoek/Agro.git)
md5sums=('SKIP')

build() {
	cd "$pkgname"
	make
}

check() {
	cd "$pkgname"
	make -k check
}

package() {
	cd "$pkgname"
	install -Dm755 ./agro "$pkgdir/usr/bin/agro"
}
