PORTNAME=	cw
PORTVERSION=	1.0.16
PORTREVISION=	2
CATEGORIES=	sysutils
MASTER_SITES=	http://cwrapper.sourceforge.net/ \
		http://www.fakehalo.us/cw/

MAINTAINER=	ports@FreeBSD.org
COMMENT=	Non-intrusive color wrapper for common commands
WWW=		https://cwrapper.sourceforge.net/

LICENSE=	GPLv2+
LICENSE_FILE=	${WRKSRC}/COPYING

USES=		shebangfix

CONFLICTS_INSTALL=	unixcw # bin/cw

SHEBANG_FILES=	def/*
SHEBANG_LANG=	cw
cw_OLD_CMD=	/cw
cw_CMD=		${PREFIX}/bin/cw

GNU_CONFIGURE=	yes
GNU_CONFIGURE_MANPREFIX=${PREFIX}/share
ALL_TARGET=	local

PORTDOCS=	CHANGES CONTRIB README

OPTIONS_DEFINE=	DOCS

post-install:
.for file in cw cwu
	@${STRIP_CMD} ${STAGEDIR}${PREFIX}/bin/${file}
.endfor

post-install-DOCS-on:
	@${MKDIR} ${STAGEDIR}${DOCSDIR}
	${INSTALL_DATA} ${PORTDOCS:S|^|${WRKSRC}/|} ${STAGEDIR}${DOCSDIR}

.include <bsd.port.mk>
