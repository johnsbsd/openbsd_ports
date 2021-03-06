# $OpenBSD: Makefile,v 1.10 2020/03/17 20:42:46 rpointel Exp $

COMMENT =	Python bindings for The Sleuth Kit (libtsk)

MODPY_EGG_VERSION = 20200117
DISTNAME =	pytsk3-${MODPY_EGG_VERSION}
PKGNAME =	py-tsk-${MODPY_EGG_VERSION}

CATEGORIES =	sysutils

HOMEPAGE =	https://github.com/py4n6/pytsk/

MAINTAINER =	Remi Pointel <rpointel@openbsd.org>

# Apache v2
PERMIT_PACKAGE =	Yes

MODULES =		lang/python 
# so that we get gawk poisoning in the sleuthkit part
MODULES += 		gnu

MODPY_PI =		Yes
MODPY_SETUPTOOLS =	Yes

FLAVORS =	python3
FLAVOR =	python3

WANTLIB += pthread talloc tsk ${MODPY_WANTLIB}

# C++11
COMPILER=	ports-clang ports-gcc

pre-configure:
		${SUBST_DATA} ${WRKSRC}/setup.py ${WRKSRC}/setup.py.new
		mv ${WRKSRC}/setup.py.new ${WRKSRC}/setup.py

LIB_DEPENDS =	sysutils/sleuthkit \
		devel/libtalloc
TEST_DEPENDS =	sysutils/py-tsk${MODPY_FLAVOR}=${MODPY_EGG_VERSION}

# it needs test_data/* in the Github repository
do-test:
	cd ${WRKSRC} && ${MODPY_BIN} run_tests.py

.include <bsd.port.mk>
