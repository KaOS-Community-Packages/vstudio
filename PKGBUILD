pkgname=vstudio
pkgver=8.0
pkgrel=1
pkgdesc="GUI Admin Tool for MySQL, MariaDB, PostgreSQL, MS SQL Server, Valentina DB and SQLite"
arch=('x86_64')
url="http://www.valentina-db.com"
license=('custom')
source=("vstudio_x64_${pkgver}_lin.deb::http://www.valentina-db.com/en/studio/download/current/vstudio_x64_lin-deb")
md5sums=('ddc71b8272339c7422a77dc650bd8eec')

package() {
  bsdtar -xf data.tar.xz -C "${pkgdir}"
  mkdir "${pkgdir}/usr/bin"
  ln -sf "/opt/VStudio/${pkgname}" "${pkgdir}/usr/bin"
  sed -i -e 's|Name=VStudio|Name=Valentina Studio|g' \
         -e 's|Exec=/opt/VStudio/vstudio %F|Exec=vstudio|g' \
         ${pkgdir}/usr/share/applications/${pkgname}.desktop
}
