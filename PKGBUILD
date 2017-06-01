# Maintainer: Terunori Togo <terut.dev+github at gmail dot com>
pkgname=heroku
pkgver=5.10.0
pkgrel=1
pkgdesc="The next generation Go/Node-based Heroku CLI"
arch=("x86_64")
url="https://github.com/heroku/cli"
license=('MIT')
depends=('git')
install="heroku.install"
source=("heroku-$pkgver.tar.gz::https://cli-assets.heroku.com/branches/stable/heroku-linux-amd64.tar.gz"
        "https://raw.githubusercontent.com/heroku/cli/master/LICENSE")
sha256sums=('0660cf00bf2d446b33b137e956f732637209739d9137b665e4403f66d1652019'
            'e068ed9f18346f1aa2a7f93fa1f40256f2c66fa206bb5d7d6f92dd646e6ede02')

package() {
  cd "$srcdir/$pkgname"

  mkdir -p "$pkgdir"/usr/lib

  cp -r "$srcdir/$pkgname" "$pkgdir"/usr/lib/
  install -Dm755 bin/heroku "$pkgdir"/usr/bin/heroku
  install -Dm644 $srcdir/LICENSE "$pkgdir"/usr/share/licenses/$pkgname/LICENSE
}
