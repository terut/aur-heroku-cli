# Maintainer: Terunori Togo <terut.dev+github at gmail dot com>
pkgname=heroku-cli
pkgver=5.9.10.8ed91c2
pkgrel=1
pkgdesc="Everything you need to get started with Heroku"
arch=("x86_64")
url="https://cli.heroku.com"
license=('MIT')
optdepends=('git')
source=("heroku-cli-$pkgver.tar.gz::https://cli-assets.heroku.com/branches/stable/heroku-linux-amd64.tar.gz")
md5sums=(SKIP)

pkgver() {
  cd "$srcdir"/heroku
  bin/heroku --version | sed -e 's/^.*\/\(.*\)\s(.*$/\1/g' -e 's/-/./g'
}

package() {
  cd "$srcdir"/heroku

  mkdir -p "$pkgdir"/usr/{lib,bin}

  cp -r "$srcdir"/heroku "$pkgdir"/usr/lib/
  install -Dm755 bin/heroku "$pkgdir"/usr/bin/
}
