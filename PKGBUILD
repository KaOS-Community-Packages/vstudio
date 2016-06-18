pkgname=vstudio
pkgver=6.5.7
pkgrel=1
pkgdesc="MySQL, MariaDB, PostgreSQL, MS SQL Server, Valentina DB and SQLite GUI Admin Tool"
arch=('x86_64')
url="http://www.valentina-db.com"
license=('custom')
depends=('glibc' 'cairo' 'gcc-libs')
source=("http://www.valentina-db.com/en/studio/download/current/vstudio_x64_lin-deb")
md5sums=('4dbb4e8425118cf6fe63c9c5ddddcce9')

package() {
  bsdtar -xf data.tar.xz -C "${pkgdir}"
  mkdir "${pkgdir}/usr/bin"
  ln -sf "/opt/VStudio/${pkgname}" "${pkgdir}/usr/bin"
  sed -i -e 's|Name=VStudio|Name=Valentina Studio|g' ${pkgdir}/usr/share/applications/${pkgname}.desktop
}
