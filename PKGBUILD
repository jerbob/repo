# Generated by gem2arch (https://github.com/anatol/gem2arch)
# Maintainer: Justin Dray <justin@dray.be>

_gemname=hiera-eyaml
pkgname=ruby-$_gemname
pkgver=2.1.0
pkgrel=1
pkgdesc='OpenSSL Encryption backend for Hiera'
arch=(any)
url='https://github.com/voxpupuli/hiera-eyaml'
license=(MIT)
depends=(ruby ruby-trollop ruby-highline-1.6)
makedepends=(ruby-rdoc)
options=(!emptydirs)
source=(https://rubygems.org/downloads/$_gemname-$pkgver.gem)
noextract=($_gemname-$pkgver.gem)
sha1sums=('ce38873934b8be6c464c6065ebd529e9f2e39bfa')

package() {
  local _gemdir="$(ruby -e'puts Gem.default_dir')"
  gem install --ignore-dependencies --no-user-install -i "$pkgdir/$_gemdir" -n "$pkgdir/usr/bin" $_gemname-$pkgver.gem
  rm "$pkgdir/$_gemdir/cache/$_gemname-$pkgver.gem"
  install -D -m644 "$pkgdir/$_gemdir/gems/$_gemname-$pkgver/LICENSE.txt" "$pkgdir/usr/share/licenses/$pkgname/LICENSE.txt"
}
