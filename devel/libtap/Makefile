PORTNAME=	libtap
PORTVERSION=	1.12.0
PORTREVISION=	1
CATEGORIES=	devel
MASTER_SITES=	https://web-cpan.shlomifish.org/downloads/

MAINTAINER=	rodrigo@FreeBSD.org
COMMENT=	Library implementing the Test Anything Protocol
WWW=		https://www.shlomifish.org/open-source/projects/libtap/

LICENSE=	BSD2CLAUSE
LICENSE_FILE=	${WRKSRC}/COPYING

USES=		cmake perl5 tar:bz2
USE_LDCONFIG=	yes
USE_PERL5=	build

TEST_TARGET=	check

.include <bsd.port.mk>
