# $OpenBSD: Makefile,v 1.31 2019/12/30 14:57:24 jasper Exp $

COMMENT=	braille translator, back-translator and formatter

V=		3.12.0
DISTNAME=	liblouis-${V}

SHARED_LIBS +=  louis                8.0      # 19.0

CATEGORIES=	devel

HOMEPAGE=	http://www.liblouis.org/

# GPLv3 - LGPLv3 - LGPLv2.1+
PERMIT_PACKAGE=	Yes

WANTLIB += c

MASTER_SITES=	https://github.com/liblouis/liblouis/releases/download/v${V}/

MODULES=	lang/python

DEBUG_PACKAGES =${BUILD_PACKAGES}

MODPY_VERSION=	${MODPY_DEFAULT_VERSION_3}

BUILD_DEPENDS=	devel/help2man

# lou_maketable
RUN_DEPENDS +=	shells/bash

CONFIGURE_STYLE=gnu
CONFIGURE_ARGS=	--with-packager="OpenBSD Ports" \
		--enable-ucs4

post-install:
	${INSTALL_DATA_DIR} ${WRKINST}/${MODPY_SITEPKG}/louis
	${INSTALL_DATA} ${WRKSRC}/python/louis/__init__.py \
		${WRKINST}/${MODPY_SITEPKG}/louis
	${MODPY_BIN} ${MODPY_LIBDIR}/compileall.py ${WRKINST}${MODPY_SITEPKG}

.include <bsd.port.mk>
