PORTNAME=	libnids
PORTVERSION=	1.24
PORTREVISION=	6
CATEGORIES=	net security
MASTER_SITES=	SF

MAINTAINER=	ports@FreeBSD.org
COMMENT?=	Network monitoring library with TCP/IP reassembly
WWW=		http://libnids.sf.net

LIB_DEPENDS=	libnet.so:net/libnet

LICENSE=	GPLv2

OPTIONS_DEFINE=	GLIB2 DOCS
OPTIONS_DEFAULT=GLIB2
GLIB2_DESC=	Use GLIB2 for multiprocessing support
OPTIONS_SUB=	yes

GLIB2_USES=	gnome
GLIB2_USE=	gnome=glib20
GLIB2_CONFIGURE_ENABLE=	libglib

USES=		cpe pkgconfig
CPE_VENDOR=	${PORTNAME}_project
GNU_CONFIGURE=	yes

do-install:
	${INSTALL_DATA} ${WRKSRC}/src/nids.h ${STAGEDIR}${PREFIX}/include
	${INSTALL_DATA} ${WRKSRC}/src/libnids.a ${STAGEDIR}${PREFIX}/lib
	${INSTALL_MAN} ${WRKSRC}/src/libnids.3 ${STAGEDIR}${PREFIX}/share/man/man3
	${MKDIR} ${STAGEDIR}${DOCSDIR}
	(cd ${WRKSRC} && ${INSTALL_DATA} README doc/* ${STAGEDIR}${DOCSDIR})

.include <bsd.port.mk>
