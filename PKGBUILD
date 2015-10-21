# Maintainer: Tim Kleinschmidt <tim.kleinschmidt@gmail.com>

pkgname=gitkraken
pkgrel=1
pkgver=0.30.8
pkgdesc="The intuitive, fast, and beautiful cross-platform Git client."
url="http://www.gitkraken.com/"
provides=('gitkraken')
arch=('x86_64')
license=('custom')
depends=('gtk2' 'nss' 'libnotify' 'libxtst' 'libgnome-keyring' 'gconf' 'gcc-libs-multilib' 'alsa-lib')
makedepends=()
backup=()
install=''
source=("https://release.gitkraken.com/linux/gitkraken-amd64.tar.gz")
md5sums=('6c15078d83302c74fb121ca2274730bf')

package() {
	install -d "$pkgdir"/opt
	cp -R "$srcdir"/GitKraken "$pkgdir"/opt/gitkraken

	find "$pkgdir"/opt/gitkraken/ -type f -exec chmod 644 {} \;
	chmod 755 "$pkgdir"/opt/gitkraken/gitkraken

	install -d "$pkgdir"/usr/bin
	ln -s ../../opt/gitkraken/gitkraken "$pkgdir"/usr/bin/gitkraken

	install -Dm644 "$srcdir"/GitKraken/LICENSE "$pkgdir"/usr/share/licenses/$pkgname/LICENSE
}
