pkgname=vstudio
pkgver=8.2
pkgrel=1
pkgdesc="GUI Admin Tool for MySQL, MariaDB, PostgreSQL, MS SQL Server, Valentina DB and SQLite"
arch=('x86_64')
url="http://www.valentina-db.com"
license=('custom')
source=("vstudio_x64_${pkgver}_lin.deb::http://www.valentina-db.com/en/studio/download/current/vstudio_x64_lin-deb")
md5sums=('36b3d73d7d0fe79d9cb680a03c27e965')

package() {
    bsdtar -xf data.tar.xz -C ${pkgdir}
    mkdir -p ${pkgdir}/usr/bin
    
    ln -sf /opt/VStudio/${pkgname} ${pkgdir}/usr/bin
    sed -i -e 's|Name=VStudio|Name=Valentina Studio|g' \
           -e 's|Exec=/opt/VStudio/vstudio %F|Exec=vstudio|g' \
           ${pkgdir}/usr/share/applications/${pkgname}.desktop
}
