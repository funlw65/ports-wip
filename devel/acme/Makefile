# $OpenBSD$

COMMENT=		ACME crossassembler for multiple environments

DISTNAME=		acme-crossass-code-0-97-trunk
PKGNAME=    		acme-0.96.4
EXTRACT_SUFX= 		.zip
WRKDIST=		${WRKDIR}/acme-crossass-code-0-97-trunk

CATEGORIES=		devel

HOMEPAGE=		http://sourceforge.net/p/acme-crossass/
PERMIT_PACKAGE_CDROM=	Yes
PERMIT_PACKAGE_FTP=	Yes
PERMIT_DISTFILES_FTP=	Yes

WANTLIB += 		c m

MASTER_SITES = 		https://sourceforge.net/code-snapshots/svn/a/ac/acme-crossass/code-0/

do-build:
	cd ${WRKSRC}/src && $(MAKE_PROGRAM) CC=cc

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/src/acme ${PREFIX}/bin/acme
	${INSTALL_DATA_DIR} ${PREFIX}/share/doc/acme
	${INSTALL_DATA} ${WRKSRC}/docs/* ${PREFIX}/share/doc/acme


.include <bsd.port.mk>
