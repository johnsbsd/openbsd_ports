# $OpenBSD: Makefile,v 1.6 2019/07/12 20:45:17 sthen Exp $

COMMENT =		finite-state machines in Python

MODPY_EGG_VERSION =	0.6.0

DISTNAME =		Automat-${MODPY_EGG_VERSION}
PKGNAME =		py-automat-${MODPY_EGG_VERSION}
REVISION =		0

CATEGORIES =		devel

HOMEPAGE =		https://github.com/glyph/Automat

# MIT
PERMIT_PACKAGE =	Yes

MODULES =		lang/python
MODPY_PI =		Yes
MODPY_SETUPTOOLS =	Yes
MODPY_PYTEST =		Yes
MODPY_PYTEST_ARGS =	lib/automat/_test/

BUILD_DEPENDS =		devel/py-setuptools_scm${MODPY_FLAVOR} \
			textproc/py-m2r${MODPY_FLAVOR}

RUN_DEPENDS =		devel/py-attrs${MODPY_FLAVOR} \
			devel/py-six${MODPY_FLAVOR} \

TEST_DEPENDS =		devel/py-twisted${MODPY_FLAVOR}

FLAVORS =		python3
FLAVOR ?=

.if ${FLAVOR:Mpython3}
TEST_DEPENDS +=		devel/py-six${MODPY_FLAVOR}
.endif

post-install:
	mv ${PREFIX}/bin/automat-visualize{,${MODPY_BIN_SUFFIX}}

.include <bsd.port.mk>
