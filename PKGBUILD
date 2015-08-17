# Maintainer: Christian Hesse <mail@eworm.de>

pkgname=perl-net-ldap-server
pkgver=0.43
pkgrel=2
pkgdesc='Perl extension for LDAP server side protocol handling'
arch=(any)
url="http://search.cpan.org/~aar/Net-LDAP-Server-${pkgver}/lib/Net/LDAP/Server.pm"
license=('perl')
source=("http://search.cpan.org/CPAN/authors/id/A/AA/AAR/Net-LDAP-Server-${pkgver}.tar.gz")
depends=('perl' 'perl-ldap' 'perl-convert-asn1')

build() {
	cd "${srcdir}/Net-LDAP-Server-${pkgver}/"

	PERL_MM_USE_DEFAULT=1 perl Makefile.PL INSTALLDIRS=vendor
	make
}

package() {
	cd "${srcdir}/Net-LDAP-Server-${pkgver}/"

	make install DESTDIR="${pkgdir}"
}

sha256sums=('dd6c4cb4d30bc32114b0787faa2a1e2b4fedd1b91c2ef37965ecba11331bb062')
