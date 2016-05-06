pkgname=vstudio
pkgver=6.5.3
pkgrel=1
pkgdesc="MySQL, MariaDB, PostgreSQL, MS SQL Server, Valentina DB and SQLite GUI Admin Tool"
arch=('x86_64')
url="http://www.valentina-db.com"
license=('custom')
depends=('glibc' 'cairo' 'gcc-libs')
source=("http://www.valentina-db.com/en/studio/download/current/vstudio_x64_lin-deb")
sha256sums=('f8442af242b0fece587945f0143865cbf76070ba1c159ae2d6a153bbb80ea5fb')

package() {
  bsdtar -xf data.tar.xz -C "${pkgdir}"
  mkdir "${pkgdir}/usr/bin"
  ln -sf "/opt/VStudio/${pkgname}" "${pkgdir}/usr/bin"
  sed -i -e 's|Name=VStudio|Name=Valentina Studio|g' ${pkgdir}/usr/share/applications/${pkgname}.desktop
}
