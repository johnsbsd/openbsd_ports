# $OpenBSD: Makefile,v 1.15 2019/12/01 02:22:12 kmos Exp $

COMMENT =		official command-line client for RIPE Atlas

MODPY_EGG_VERSION =	2.3.0
DISTNAME =		ripe.atlas.tools-${MODPY_EGG_VERSION}
REVISION =		0

CATEGORIES =		net

HOMEPAGE =		https://github.com/RIPE-NCC/ripe-atlas-tools

MAINTAINER =		Stuart Henderson <sthen@openbsd.org>

# GPLv3
PERMIT_PACKAGE =	Yes

MODPY_PI =		Yes
MODPY_SETUPTOOLS =	Yes
MODPY_PYTEST =		Yes
MODPY_PYTEST_ARGS =	tests/test*.py tests/*/*.py

MODULES =		lang/python

PORTHOME =		${WRKDIST}

MODPY_VERSION =		${MODPY_DEFAULT_VERSION_3}

RUN_DEPENDS =		devel/py-dateutil${MODPY_FLAVOR} \
			devel/py-tzlocal${MODPY_FLAVOR} \
			net/py-IP${MODPY_FLAVOR} \
			net/py-ripe.atlas.cousteau${MODPY_FLAVOR} \
			net/py-ripe.atlas.sagan${MODPY_FLAVOR} \
			security/py-openssl${MODPY_FLAVOR} \
			textproc/py-yaml${MODPY_FLAVOR} \
			www/py-requests${MODPY_FLAVOR}

TEST_DEPENDS =		devel/py-coverage${MODPY_FLAVOR} \
			devel/py-mock${MODPY_FLAVOR} \
			devel/py-nose${MODPY_FLAVOR}

.include <bsd.port.mk>
