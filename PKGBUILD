pkgname=wordpress-desktop
pkgver=1.7.0
pkgrel=1
pkgdesc="A desktop app that gives WordPress a permanent home in your dock"
arch=('x86_64')
url="https://desktop.wordpress.com/"
license=('GPLv2')
depends=('systemd' 'gconf' 'gtk2' 'nss' 'alsa-lib' 'libxtst' 'libnotify' 'fontconfig')
sha256sums=('b216d647e06433f70b6bb814f91b68c9769d433470e51fb70815ff9c4043486b')
source=("https://public-api.wordpress.com/rest/v1.1/desktop/linux/download?type=deb")

package() {
  tar -xzf ${srcdir}/data.tar.gz -C "${pkgdir}"
  chmod -R 755 "$pkgdir/usr"
  rm -rf ${pkgdir}/usr/share/doc
  install -dm755 ${pkgdir}/usr/bin
  ln -s /usr/share/wpcom/wpcom ${pkgdir}/usr/bin/${pkgname}
}
