# no RCS Id here, please

COMMENT =	portbump test package 6
PKGNAME =	portbump-t6-1.0

WANTLIB =	c m

DISTFILES =

do-extract:
	cp ${FILESDIR}/{Makefile,*.c} ${WRKSRC}

do-install:
	${INSTALL_PROGRAM} ${WRKBUILD}/t6 ${PREFIX}/bin

.include <bsd.port.mk>
