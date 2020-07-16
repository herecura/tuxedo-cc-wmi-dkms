# Maintainer: Steven Seifried <gitlab@canox.net>
# Contributor: Steven Seifried <gitlab@canox.net>
_pkgname=tuxedo-cc-wmi
pkgname=tuxedo-cc-wmi-dkms
pkgver=0.1.4
pkgrel=1
pkgdesc="WMI method control for TUXEDO laptops"
arch=(x86_64)
url="https://github.com/tuxedocomputers/tuxedo-cc-wmi"
license=('GPL3')
depends=('dkms')
optdepends=('linux-headers: build modules against Arch kernel'
            'linux-lts-headers: build modules against LTS kernel'
            'linux-zen-headers: build modules against ZEN kernel'
            'linux-hardened-headers: build modules against the HARDENED kernel')
conflicts=('tuxedo-wmi' 'tuxedo-wmi-dkms')
provides=('tuxedo-cc-wmi')
source=("$_pkgname-$pkgver.tar.gz::https://github.com/tuxedocomputers/tuxedo-cc-wmi/archive/v0.1.4.tar.gz")
sha512sums=('a41faa7290859410eb8446dd02ee2bdf87a3085882f3fc6b968701bb14bab87bd6bcd4bf9839111c62eab8a8751f8c2cf378aa7297879f7781f73998199e5f27')

package() {
  tar -vxzf "$_pkgname-$pkgver.tar.gz"
  mkdir -p "$pkgdir/usr/src/$_pkgname-$pkgver"
  cp -r "$srcdir/$_pkgname-$pkgver"/* "$pkgdir/usr/src/$_pkgname-$pkgver"
  install -D "$srcdir/$_pkgname-$pkgver/dkms.conf" "$pkgdir/usr/src/$_pkgname-$pkgver/dkms.conf"
}
