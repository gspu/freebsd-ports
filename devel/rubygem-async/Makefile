PORTNAME=	async
PORTVERSION=	2.21.1
CATEGORIES=	devel rubygems
MASTER_SITES=	RG

MAINTAINER=	sunpoet@FreeBSD.org
COMMENT=	Modern asynchronous I/O framework for Ruby
WWW=		https://socketry.github.io/async/ \
		https://github.com/socketry/async

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/license.md

RUN_DEPENDS=	rubygem-console>=1.29<2:devel/rubygem-console \
		rubygem-fiber-annotation>=0:devel/rubygem-fiber-annotation \
		rubygem-io-event>=1.6.5<2:devel/rubygem-io-event

USES=		gem

NO_ARCH=	yes

.include <bsd.port.mk>
