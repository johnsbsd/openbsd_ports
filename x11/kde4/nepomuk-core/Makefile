# $OpenBSD: Makefile,v 1.15 2020/05/14 19:16:25 rsadowski Exp $

COMMENT =	KDE Nepomuk core libraries
DISTNAME =	nepomuk-core-${MODKDE4_VERSION}
REVISION =	4

SHARED_LIBS =	nepomukcore		53.0 # 4.9
SHARED_LIBS +=	nepomukcommon		53.0 # 4.10
SHARED_LIBS +=	kdeinit4_nepomukserver	53.0 # 4.10
SHARED_LIBS +=	nepomukextractor	53.0
SHARED_LIBS +=	nepomukcleaner		1.0

WANTLIB =  c m pthread
WANTLIB += ${COMPILER_LIBCXX}
WANTLIB += lib/qt4/QtDBus lib/qt4/QtGui lib/qt4/QtNetwork lib/qt4/QtSvg
WANTLIB += lib/qt4/QtXml
WANTLIB += ${KDE4LIB}/baloocore ${KDE4LIB}/baloofiles ${KDE4LIB}/baloopim
WANTLIB += ${KDE4LIB}/balooqueryparser
WANTLIB += ${KDE4LIB}/kdeui ${KDE4LIB}/kidletime ${KDE4LIB}/kio
WANTLIB += ${KDE4LIB}/solid
WANTLIB += avcodec avformat avutil epub exiv2 soprano
WANTLIB += sopranoserver tag

MODKDE4_USE =	libs

BUILD_DEPENDS =	misc/shared-desktop-ontologies>=0.10.51

RUN_DEPENDS =	devel/desktop-file-utils \
		misc/shared-desktop-ontologies>=0.10.51

LIB_DEPENDS =	audio/taglib \
		databases/soprano>=2.9.3 \
		graphics/exiv2 \
		graphics/ffmpeg \
		textproc/ebook-tools \
		${MODKDE4_DEP_DIR}/baloo>=${MODKDE4_DEP_VERSION}

CONFIGURE_ARGS =	-DCMAKE_DISABLE_FIND_PACKAGE_QMobipocket=True \
			-DCMAKE_DISABLE_FIND_PACKAGE_Doxygen=True \
			-DCMAKE_DISABLE_FIND_PACKAGE_PopplerQt4=True

.include <bsd.port.mk>
