pkgname=vstudio
pkgver=13.9
pkgrel=1
pkgdesc="GUI Admin Tool for MySQL, MariaDB, PostgreSQL, MS SQL Server, Valentina DB and SQLite"
arch=('x86_64')
url="http://www.valentina-db.com"
license=('custom')
source=("vstudio_x64_${pkgver}_lin.deb::https://valentina-db.com/en/all-downloads/vstudio/current/vstudio_x64_lin_deb")
md5sums=('16a0d9645cd03b80aaffa8bf8963ac8b')

package() {
    bsdtar -xf data.tar.xz -C ${pkgdir}
    mkdir -p ${pkgdir}/usr/bin
    
    ln -sf /opt/VStudio/${pkgname} ${pkgdir}/usr/bin
    sed -i -e 's|Name=VStudio|Name=Valentina Studio|g' \
           -e 's|Exec=/opt/VStudio/vstudio %F|Exec=/usr/bin/vstudio|g' \
           ${pkgdir}/usr/share/applications/${pkgname}.desktop
}
