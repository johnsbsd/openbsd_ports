# $OpenBSD: Makefile,v 1.4 2020/05/16 11:16:09 sthen Exp $

COMMENT =		programmable completion functions for bash

GH_PROJECT =		bash-completion
GH_ACCOUNT =		scop
GH_TAGNAME =		2.10
REVISION =		1

CATEGORIES =		shells sysutils

# GPLv2
PERMIT_PACKAGE =	Yes

MODULES =		lang/python
MODPY_VERSION =		${MODPY_DEFAULT_VERSION_3}
MODPY_RUNDEP =		No

BUILD_DEPENDS =		shells/bash
TEST_DEPENDS =		devel/dejagnu \
			devel/py-pexpect${MODPY_FLAVOR} \
			devel/py-test${MODPY_FLAVOR}

USE_GMAKE =		Yes

AUTOCONF_VERSION =	2.69
AUTOMAKE_VERSION =	1.16
CONFIGURE_STYLE =	autoreconf
CONFIGURE_ENV =		PYTEST=py.test${MODPY_BIN_SUFFIX}

FAKE_FLAGS =		sysconfdir=${PREFIX}/share/examples/bash-completion/

.include <bsd.port.mk>
