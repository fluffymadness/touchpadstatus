# Maintainer:  fluffymadness
# fluffymadness(at)posteo.de

pkgname=touchpadstatus-git
_gitname=touchpadstatus
pkgver=923f444
pkgrel=1
pkgdesc="Sentellic (Quanta TW9) Touchpad Indicator that deactivates the touchpad when a mouse is connected"
arch=('i686' 'x86_64')
url="https://github.com/fluffymadness/touchpadstatus"
license=('GPLv2')
depends=('python2' 'python2-pyqt4')
makedepends=('git')
# The git repo is detected by the 'git:' or 'git+' beginning. The branch
# 'pacman41' is then checked out upon cloning, expediating versioning:
#source=('git+https://github.com/falconindy/expac.git'
source=('git://github.com/fluffymadness/touchpadstatus.git')
# Because the sources are not static, skip Git checksum:
md5sums=('SKIP')

pkgver() {
  cd $_gitname
  # Use the tag of the last commit
  git describe --always | sed 's|-|.|g'
}



package() {
  cd $_gitname
  install -Dm755 "touchpadstatus.py" "$pkgdir/usr/bin/touchpadstatus"
  install -Dm755 "icons/touchpadstatus-active.png" "$pkgdir/usr/share/pixmaps/touchpadstatus-active.png"
  install -Dm755 "icons/touchpadstatus-inactive.png" "$pkgdir/usr/share/pixmaps/touchpadstatus-inactive.png"
}
