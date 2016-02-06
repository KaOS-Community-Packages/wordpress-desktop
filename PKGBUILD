pkgname=wordpress-desktop
pkgver=1.2.5
pkgrel=1
pkgdesc="A desktop app that gives WordPress a permanent home in your dock"
arch=('x86_64')
url="https://desktop.wordpress.com/"
license=('GPLv2')
sha256sums=('31590e9fdd999e39aa63fea5e4b3d22996dabfa1c700b96623a7b3fec355afab')
source=("https://public-api.wordpress.com/rest/v1.1/desktop/linux/download?type=deb")

package() {
  tar -xzf ${srcdir}/data.tar.gz -C "${pkgdir}"
}
