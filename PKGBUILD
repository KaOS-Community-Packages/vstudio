pkgname=vstudio
pkgver=7.5.4
pkgrel=1
pkgdesc="MySQL, MariaDB, PostgreSQL, MS SQL Server, Valentina DB and SQLite GUI Admin Tool"
arch=('x86_64')
url="http://www.valentina-db.com"
license=('custom')
depends=('glibc' 'cairo' 'gcc-libs')
source=("vstudio_x64_${pkgver}_lin.deb::http://www.valentina-db.com/en/studio/download/current/vstudio_x64_lin-deb")
md5sums=('5b16272d9077204c7d40087e7e9ec841')

package() {
  bsdtar -xf data.tar.xz -C "${pkgdir}"
  mkdir "${pkgdir}/usr/bin"
  ln -sf "/opt/VStudio/${pkgname}" "${pkgdir}/usr/bin"
  sed -i -e 's|Name=VStudio|Name=Valentina Studio|g' ${pkgdir}/usr/share/applications/${pkgname}.desktop
}
