pkgname=vstudio
pkgver=6.3.5
pkgrel=1
pkgdesc="MySQL, MariaDB, PostgreSQL, MS SQL Server, Valentina DB and SQLite GUI Admin Tool"
arch=('x86_64')
url="http://www.valentina-db.com"
license=('custom')
depends=('glibc' 'cairo' 'gcc-libs')
source=("vstudio-${pkgver%.*}-x86_64-linux.deb::http://www.valentina-db.com/en/studio/download/current/vstudio_x64_lin-deb")
sha256sums=('0e2789bb87a80ea6890c41508ebe773989c161e5cd2ec26f7d43e50710395822')

package() {
  bsdtar -xf data.tar.xz -C "${pkgdir}"
  mkdir "${pkgdir}/usr/bin"
  ln -sf "/opt/VStudio/${pkgname}" "${pkgdir}/usr/bin"
}
