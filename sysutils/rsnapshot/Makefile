PORTNAME=	rsnapshot
PORTVERSION=	1.4.4
PORTREVISION=	2
CATEGORIES=	sysutils
MASTER_SITES=	http://www.rsnapshot.org/downloads/

MAINTAINER=	ralfvd@gmail.com
COMMENT=	Filesystem snapshot utility based on rsync(1)
WWW=		https://www.rsnapshot.org

LICENSE=	GPLv2+
LICENSE_FILE=	${WRKSRC}/COPYING

BUILD_DEPENDS=	rsync:net/rsync
RUN_DEPENDS=	rsync:net/rsync \
		p5-Lchown>=0:sysutils/p5-Lchown

USES=		perl5

GNU_CONFIGURE=	yes
GNU_CONFIGURE_MANPREFIX=${PREFIX}/share
NO_ARCH=	yes

PORTDOCS=	AUTHORS ChangeLog README.md

OPTIONS_DEFINE=	DOCS

post-install-DOCS-on:
	@${MKDIR} ${STAGEDIR}${DOCSDIR}
	cd ${WRKSRC} && ${INSTALL_DATA} ${PORTDOCS} ${STAGEDIR}${DOCSDIR}

.include <bsd.port.mk>
