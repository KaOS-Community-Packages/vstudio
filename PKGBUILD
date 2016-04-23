pkgname=vstudio
pkgver=6.5.1
pkgrel=1
pkgdesc="MySQL, MariaDB, PostgreSQL, MS SQL Server, Valentina DB and SQLite GUI Admin Tool"
arch=('x86_64')
url="http://www.valentina-db.com"
license=('custom')
depends=('glibc' 'cairo' 'gcc-libs')
source=("http://www.valentina-db.com/en/studio/download/current/vstudio_x64_lin-deb")
sha256sums=('52d0b4bfcf385decf3a2f3173d5c332f3b9b9430dcb5dec43cb834065b7d77a1')

package() {
  bsdtar -xf data.tar.xz -C "${pkgdir}"
  mkdir "${pkgdir}/usr/bin"
  ln -sf "/opt/VStudio/${pkgname}" "${pkgdir}/usr/bin"

  sed -i -e 's|Name=VStudio|Name=Valentina Studio|g' ${pkgdir}/usr/share/applications/${pkgname}.desktop

}
