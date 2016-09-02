pkgname=wordpress-desktop
pkgver=1.6.0
pkgrel=1
pkgdesc="A desktop app that gives WordPress a permanent home in your dock"
arch=('x86_64')
url="https://desktop.wordpress.com/"
license=('GPLv2')
depends=('systemd' 'gconf' 'gtk2' 'nss' 'alsa-lib' 'libxtst' 'libnotify' 'fontconfig')
sha256sums=('a28274d40b97596169d3bdc920e2db2e386b96ccc34143a86a5cc4e646a4b902')
source=("https://public-api.wordpress.com/rest/v1.1/desktop/linux/download?type=deb")

package() {
  tar -xzf ${srcdir}/data.tar.gz -C "${pkgdir}"
  chmod -R 755 "$pkgdir/usr"
  rm -rf ${pkgdir}/usr/share/doc
  install -dm755 ${pkgdir}/usr/bin
  ln -s /usr/share/wpcom/wpcom ${pkgdir}/usr/bin/${pkgname}
}
