pkgname=vstudio
pkgver=8.6.3
pkgrel=1
pkgdesc="GUI Admin Tool for MySQL, MariaDB, PostgreSQL, MS SQL Server, Valentina DB and SQLite"
arch=('x86_64')
url="http://www.valentina-db.com"
license=('custom')
source=("vstudio_x64_${pkgver}_lin.deb::http://www.valentina-db.com/en/studio/download/current/vstudio_x64_lin-deb")
md5sums=('f5802e348ad83e82a1402eb9e6a36703')

package() {
    bsdtar -xf data.tar.xz -C ${pkgdir}
    mkdir -p ${pkgdir}/usr/bin
    
    ln -sf /opt/VStudio/${pkgname} ${pkgdir}/usr/bin
    sed -i -e 's|Name=VStudio|Name=Valentina Studio|g' \
           -e 's|Exec=/opt/VStudio/vstudio %F|Exec=vstudio|g' \
           ${pkgdir}/usr/share/applications/${pkgname}.desktop
}
