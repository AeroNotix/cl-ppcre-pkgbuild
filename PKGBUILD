# Maintainer: Aaron France <aaron.l.france@gmail.com>
# Contributor: veox <cy at wre dot ath dot cx>
# Contributor: joyfulgirl <joyfulgirl (at) archlinux.us>
# Contributor: Jonathan Friedman <jonf@gojon.com>
# Contributor: Aaron France <aaron.l.france@gmail.com>
pkgname=cl-ppcre
pkgver=2.0.9
pkgrel=2
pkgdesc="Perl-compatible, portable regexp library for Common Lisp"
arch=('i686' 'x86_64')
url="http://www.weitz.de/cl-ppcre/"
license=('BSD')

depends=('common-lisp' 'cl-asdf')

install=cl-ppcre.install
source=('http://weitz.de/files/cl-ppcre.tar.gz' 'LICENSE')
md5sums=('267c77ddb8cd55247bf29bb31b1fefcb'
         'c6aa01dce26b45aa916329701a448d11')

package() {
    install -d ${pkgdir}/usr/share/common-lisp/source/${pkgname}
    install -d ${pkgdir}/usr/share/common-lisp/systems
    install -d ${pkgdir}/usr/share/licenses/${pkgname}

    cd ${srcdir}/${pkgname}-${pkgver}

    install -m 644 -t ${pkgdir}/usr/share/common-lisp/source/${pkgname} \
        ${srcdir}/${pkgname}-${pkgver}/*.lisp
    install -m 644 -t ${pkgdir}/usr/share/common-lisp/source/${pkgname} \
        ${srcdir}/${pkgname}-${pkgver}/*.asd
    install -m 644 ${srcdir}/LICENSE \
        ${pkgdir}/usr/share/licenses/${pkgname}

    cd ${pkgdir}/usr/share/common-lisp/systems
    ln -s ../source/${pkgname}/${pkgname}.asd .
    ln -s ../source/${pkgname}/${pkgname}-unicode.asd .
}

# vim:set ts=2 sw=4 et nospell:
