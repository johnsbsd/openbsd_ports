# $OpenBSD: Makefile,v 1.6 2020/03/23 18:01:14 rsadowski Exp $

COMMENT =	arcade bombing game
DISTNAME =	bomber-${VERSION}
CATEGORIES =	games

HOMEPAGE =	https://www.kde.org/applications/education/bomber/

WANTLIB += ${COMPILER_LIBCXX} KF5Auth KF5AuthCore KF5Codecs KF5ConfigCore
WANTLIB += KF5ConfigGui KF5ConfigWidgets KF5CoreAddons KF5Crash
WANTLIB += KF5DBusAddons KF5I18n KF5KDEGames KF5WidgetsAddons
WANTLIB += KF5XmlGui Qt5Core Qt5DBus Qt5Gui Qt5Network Qt5Qml
WANTLIB += Qt5Quick Qt5QuickWidgets Qt5Widgets Qt5Xml c m

MODKDE5_DESKTOP_FILE = yes
MODKDE5_ICON_CACHE = yes
MODKDE5_TRANSLATIONS = yes
MODKDE5_DOCS = yes

MODULES +=	x11/kde-applications

BUILD_DEPENDS =	x11/qt5/qtquickcontrols \
		x11/qt5/qtsvg
RUN_DEPENDS =	x11/qt5/qtquickcontrols \
		x11/qt5/qtsvg

LIB_DEPENDS =	devel/kf5/kauth \
		devel/kf5/kcodecs \
		devel/kf5/ki18n \
		devel/kf5/kcrash \
		devel/kf5/kdbusaddons \
		devel/kf5/kconfig \
		devel/kf5/kcoreaddons \
		devel/kf5/kxmlgui \
		x11/qt5/qtdeclarative \
		x11/kde-applications/libkdegames

.include <bsd.port.mk>
