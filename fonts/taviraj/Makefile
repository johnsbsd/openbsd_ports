# $OpenBSD: Makefile,v 1.2 2019/07/12 20:46:13 sthen Exp $

COMMENT =	Serif Latin and Looped Thai typeface

DISTNAME =	taviraj-0.20160412

GH_ACCOUNT =	cadsondemak
GH_PROJECT =	taviraj
GH_COMMIT =	8bd077c195dccf3bfc4699ec6ae9c6909bdd03a5

CATEGORIES =	fonts

HOMEPAGE =	https://cadsondemak.github.io/taviraj/

MAINTAINER =	George Rosamond <george@nycbug.org>

# SIL OFL 1.1
PERMIT_PACKAGE =	Yes

NO_BUILD =		Yes
NO_TEST =		Yes

FONTDIR =		${PREFIX}/share/fonts/taviraj
DOCDIR =		${PREFIX}/share/doc/taviraj

do-install:
	${INSTALL_DATA_DIR} ${FONTDIR} ${DOCDIR}
	${INSTALL_DATA} ${WRKDIST}/font/{*.otf,*.ttf} ${FONTDIR}
	${INSTALL_DATA} ${WRKDIST}/{OFL.txt,README.md} ${DOCDIR}

.include <bsd.port.mk>
