# Maintainer: Thomas Wood <grand.edgemaster@gmail.com>
pkgname=twemoji-color-font
pkgver=1.1
pkgrel=1
pkgdesc="A color and B&W emoji SVG-in-OpenType font with support for ZWJ, skin tone modifiers and country flags."
arch=('any')
url="https://github.com/eosrei/twemoji-color-font"
license=('custom:CCPL:by-4.0' 'MIT')

# ttf-bitstream-vera is required for bug-free font fallback with the provided fontconfig.
# Please don't complain about it. See: https://github.com/eosrei/emojione-color-font#why-bitstream-vera
depends=(fontconfig ttf-bitstream-vera)

_pkgver=${pkgver//_/-}
_archive=TwitterColorEmoji-SVGinOT-Linux-${_pkgver}

source=(
  "https://github.com/eosrei/$pkgname/releases/download/v${_pkgver}/${_archive}.tar.gz"
)
install=$pkgname.install

_srcdir=${pkgname}-${_pkgver}

package() {
  cd ${_archive}
  install -Dm644 TwitterColorEmoji-SVGinOT.ttf -t "$pkgdir"/usr/share/fonts/"Twitter Color Emoji"/
  install -Dm644 LICENSE* -t "$pkgdir"/usr/share/licenses/$pkgname/
  install -Dm644 README.md "$pkgdir"/usr/share/doc/$pkgname/README
  install -Dm644 fontconfig/56-twemoji-color.conf "$pkgdir"/etc/fonts/conf.avail/56-$pkgname.conf
}

md5sums=('d7e572086387c1944bc497776ffc1d75')
