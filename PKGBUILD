pkgname=wordpress-desktop
pkgver=1.3.1
pkgrel=1
pkgdesc="A desktop app that gives WordPress a permanent home in your dock"
arch=('x86_64')
url="https://desktop.wordpress.com/"
license=('GPLv2')
depends=('systemd' 'gconf' 'gtk2' 'nss' 'alsa-lib' 'libxtst' 'libnotify' 'fontconfig')
sha256sums=('68dd92a78195905291e8ca6ef5931e29a63344b9c6291dcd34059a236f4e59b6')
source=("https://public-api.wordpress.com/rest/v1.1/desktop/linux/download?type=deb")

package() {
  tar -xzf ${srcdir}/data.tar.gz -C "${pkgdir}"
  chmod -R 755 "$pkgdir/usr"
  rm -rf ${pkgdir}/usr/share/doc
  install -dm755 ${pkgdir}/usr/bin
  ln -s ${pkgdir}/usr/share/wpcom/wpcom ${pkgdir}/usr/bin/${pkgname}
}
