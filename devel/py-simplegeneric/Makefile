# $OpenBSD: Makefile,v 1.8 2019/07/12 20:45:53 sthen Exp $

COMMENT =		simple generic functions

MODPY_EGG_VERSION =	0.8.1
DISTNAME =		simplegeneric-${MODPY_EGG_VERSION}
EXTRACT_SUFX =		.zip
PKGNAME =		py-${DISTNAME}
REVISION =		4

CATEGORIES =		devel

# ZPL 2.1
# If we patch anything, we must include:
#     "prominent notices stating that you changed the files and
#     the date of any change."
PERMIT_PACKAGE =	Yes

MODULES =		lang/python
MODPY_PI =		Yes
MODPY_SETUPTOOLS =	Yes

FLAVORS =		python3
FLAVOR ?=

.include <bsd.port.mk>
