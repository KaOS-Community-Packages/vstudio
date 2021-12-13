pkgname=vstudio
pkgver=11.5.2
pkgrel=1
pkgdesc="GUI Admin Tool for MySQL, MariaDB, PostgreSQL, MS SQL Server, Valentina DB and SQLite"
arch=('x86_64')
url="http://www.valentina-db.com"
license=('custom')
source=("vstudio_x64_${pkgver}_lin.deb::https://valentina-db.com/en/all-downloads/vstudio/current/vstudio_x64_lin-deb")
md5sums=('53d90d8b54bcef64e3ba55dacde89627')

package() {
    bsdtar -xf data.tar.xz -C ${pkgdir}
    mkdir -p ${pkgdir}/usr/bin
    
    ln -sf /opt/VStudio/${pkgname} ${pkgdir}/usr/bin
    sed -i -e 's|Name=VStudio|Name=Valentina Studio|g' \
           -e 's|Exec=/opt/VStudio/vstudio %F|Exec=/usr/bin/vstudio|g' \
           ${pkgdir}/usr/share/applications/${pkgname}.desktop
}
