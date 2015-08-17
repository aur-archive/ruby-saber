# Maintainer: Guten Ye

_gemname=saber
pkgname=ruby-$_gemname
pkgver=1.0.1
pkgrel=1
pkgdesc="A complete solution for PT users."
arch=('any')
url="http://github.com/GutenYe/saber"
license=('MIT')
depends=('ruby' 'ruby-pd' 'ruby-tagen' 'ruby-optimism' 'ruby-pa' 'ruby-retort' 'ruby-thor' 'ruby-net-ssh' 'ruby-xmpp4r' 'ruby-mechanize' 'ruby-highline' 'ruby-reverse_markdown')
makedepends=('rubygems')
source=(http://rubygems.org/downloads/$_gemname-$pkgver.gem)
noextract=($_gemname-$pkgver.gem)

package() {
  cd "$srcdir"
  local _gemdir="$(ruby -e'puts Gem.default_dir')"

	mkdir -p "$pkgdir/usr/bin"
  GEM_BINDIR="$pkgdir/usr/bin" gem install --ignore-dependencies --no-user-install -i "$pkgdir$_gemdir" -n "$pkgdir/usr/bin" $_gemname-$pkgver.gem
}

md5sums=('f5abff71b3d75af03a7b4ec2be879e3f')
