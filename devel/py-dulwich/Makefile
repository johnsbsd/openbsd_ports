# $OpenBSD: Makefile,v 1.36 2020/05/17 20:20:08 millert Exp $

COMMENT =		pure Python implementation of Git file formats and protocols

MODPY_EGG_VERSION =	0.19.16
DISTNAME =		dulwich-${MODPY_EGG_VERSION}
PKGNAME =		py-${DISTNAME}

CATEGORIES =		devel

HOMEPAGE =		https://www.dulwich.io/

# GPLv2
PERMIT_PACKAGE =	Yes

WANTLIB += pthread ${MODPY_WANTLIB}

MODULES =		lang/python
MODPY_PI =		Yes
MODPY_SETUPTOOLS =	Yes

FLAVORS =		python3
FLAVOR =		python3

RUN_DEPENDS =		net/py-geventhttpclient${MODPY_FLAVOR}

TEST_DEPENDS =		devel/git,-main \
			devel/py-fastimport${MODPY_FLAVOR} \
			devel/py-greenlet${MODPY_FLAVOR} \
			devel/py-mock${MODPY_FLAVOR}

MAKE_ENV +=		LC_CTYPE=en_US.UTF-8
GIT =			${LOCALBASE}/bin/git

pre-test:
	sed -i '/^_DEFAULT_GIT/s/git/${GIT:S/\//\\\//g}/' \
		${WRKSRC}/dulwich/tests/compat/utils.py

post-install:
	rm -R ${PREFIX}/lib/python${MODPY_VERSION}/site-packages/docs
	${INSTALL_DATA_DIR} ${PREFIX}/share/doc/dulwich/tutorial
	${INSTALL_DATA} ${WRKSRC}/docs/tutorial/*.txt \
			${PREFIX}/share/doc/dulwich/tutorial

.include <bsd.port.mk>
