PORTNAME=	Term-Choose-Util
PORTVERSION=	0.146
CATEGORIES=	devel perl5
MASTER_SITES=	CPAN
PKGNAMEPREFIX=	p5-

MAINTAINER=	sunpoet@FreeBSD.org
COMMENT=	CLI related functions
WWW=		https://metacpan.org/release/Term-Choose-Util

LICENSE=	ART10 GPLv1+
LICENSE_COMB=	dual
LICENSE_FILE=	${WRKSRC}/LICENSE

BUILD_DEPENDS=	${RUN_DEPENDS}
RUN_DEPENDS=	p5-Encode-Locale>=0:converters/p5-Encode-Locale \
		p5-File-HomeDir>=0:devel/p5-File-HomeDir \
		p5-Term-Choose>=1.775:devel/p5-Term-Choose

USES=		perl5
USE_PERL5=	configure

NO_ARCH=	yes

.include <bsd.port.mk>
