# $OpenBSD: Makefile,v 1.5 2019/07/12 20:50:49 sthen Exp $

COMMENT =		compile a log format string to perl-code

MODULES =		cpan
PKG_ARCH =		*
DISTNAME =		Apache-LogFormat-Compiler-0.35
CATEGORIES =		www

# Perl
PERMIT_PACKAGE =	Yes

CONFIGURE_STYLE =	modbuild tiny

RUN_DEPENDS =		devel/p5-POSIX-strftime-Compiler>=0.30

TEST_DEPENDS =		devel/p5-Test-MockTime \
			devel/p5-Test-Requires \
			devel/p5-Try-Tiny>=0.12 \
			www/p5-HTTP-Message \
			www/p5-URI>=1.60

.include <bsd.port.mk>
