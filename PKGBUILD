# Maintainer Stefan Tatschner <stefan@sevenbyte.org>

pkgname=roundcube-sieverules
_pkgname=Roundcube-Plugin-SieveRules-Managesieve
pkgver=2.2
pkgrel=1
pkgdesc="Allows managing sieve rules in roundcube"
arch=('any')
url="https://github.com/JohnDoh/Roundcube-Plugin-SieveRules-Managesieve"
license=('GPL')
depends=('roundcubemail')
backup=('etc/webapps/roundcubemail/plugins/sieverules/config.inc.php')
source=("https://github.com/JohnDoh/Roundcube-Plugin-SieveRules-Managesieve/archive/${pkgver}.tar.gz")
md5sums=('6ea1184ef4fcf63d914312b4b671b0f1')

package() {
  mkdir -p ${pkgdir}/usr/share/webapps/roundcubemail/plugins
  mkdir -p ${pkgdir}/etc/webapps/roundcubemail/plugins/sieverules

  cd ${pkgdir}/usr/share/webapps/roundcubemail/plugins
  cp -ra ${srcdir}/${_pkgname}-${pkgver} sieverules

  cd sieverules
  cp config.inc.php.dist ${pkgdir}/etc/webapps/roundcubemail/plugins/sieverules/config.inc.php
  ln -s /etc/webapps/roundcubemail/plugins/sieverules/config.inc.php config.inc.php
}
