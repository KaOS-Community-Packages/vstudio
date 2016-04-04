pkgname=vstudio
pkgver=6.4.1
pkgrel=1
pkgdesc="MySQL, MariaDB, PostgreSQL, MS SQL Server, Valentina DB and SQLite GUI Admin Tool"
arch=('x86_64')
url="http://www.valentina-db.com"
license=('custom')
depends=('glibc' 'cairo' 'gcc-libs')
source=("vstudio-${pkgver%.*}-x86_64-linux.deb::http://www.valentina-db.com/en/studio/download/current/vstudio_x64_lin-deb")
sha256sums=('e7e1586ef089cf562536c65a97e7be614f26cf07f1d102b6a82ac5ae0bc0967a')

package() {
  bsdtar -xf data.tar.xz -C "${pkgdir}"
  mkdir "${pkgdir}/usr/bin"
  ln -sf "/opt/VStudio/${pkgname}" "${pkgdir}/usr/bin"
}
