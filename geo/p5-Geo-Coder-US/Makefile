# $OpenBSD: Makefile,v 1.9 2019/07/12 20:46:30 sthen Exp $

COMMENT=	geocode any US address
MODULES=	cpan
PKG_ARCH=	*
DISTNAME=	Geo-Coder-US-1.00
REVISION=	1
CATEGORIES=	geo

# Perl
PERMIT_PACKAGE=	Yes

RUN_DEPENDS=	geo/p5-Geo-Fips55 \
		geo/p5-Geo-StreetAddress-US \
		geo/p5-Geo-TigerLine

MODCPAN_EXAMPLES=	Yes
MODCPAN_EXAMPLES_DIST=	eg

.include <bsd.port.mk>
