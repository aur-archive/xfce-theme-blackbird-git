# Maintainer: Diego <cdprincipe at gmaildot com>

pkgname=xfce-theme-blackbird-git
pkgver=0.4
pkgrel=1
pkgdesc="A dark, ink black Xfce theme, based off of Greybird"
arch=('any')
url="https://github.com/shimmerproject/Blackbird"
license=('GPL2' 'CCPL')
depends=('gtk-engine-murrine')
makedepends=('git')
provides=('xfce-theme-blackbird')
conflicts=('xfce-theme-blackbird')
source=('git://github.com/shimmerproject/Blackbird.git')
md5sums=('SKIP')

pkgver() {
  cd Blackbird
  git describe --always | sed 's#-#_#g;s#v##'
}

package() {
  cd Blackbird
  
  # create theme dirs
  install -d -m 755 "$pkgdir"/usr/share/themes/Blackbird

  # clean up
  rm -rf {.git,.gitignore,CREDITS,LICENSE,README}

  # install theme
  cp -r . "$pkgdir"/usr/share/themes/Blackbird/

}
