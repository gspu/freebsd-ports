PORTNAME=	ftwin
PORTVERSION=	0.8.10
PORTREVISION=	1
CATEGORIES=	sysutils

MAINTAINER=	shoesoft@gmx.net
COMMENT=	Useful tool to find duplicate files
WWW=		https://github.com/fpesce/ftwin

LICENSE=	APACHE20
LICENSE_FILE=	${WRKSRC}/LICENSE

LIB_DEPENDS=	libapr-1.so:devel/apr1 \
		libexpat.so:textproc/expat2 \
		libgdbm.so:databases/gdbm \
		libgd.so:graphics/gd \
		libpcre.so:devel/pcre \
		libpuzzle.so:graphics/libpuzzle

USES=		autoreconf bdb libarchive pkgconfig tar:bzip2
GNU_CONFIGURE=	yes
GNU_CONFIGURE_MANPREFIX=${PREFIX}/share
CONFIGURE_ARGS=	--with-archive=${LOCALBASE}
USE_GITHUB=	yes
GH_ACCOUNT=	fpesce
GH_TAGNAME=	3355fd9
MAKE_ARGS=	CFLAGS="${CFLAGS}"

PORTDOCS=	AUTHORS EXAMPLES TODO CHANGES KNOWN_BUGS VERSION README
PLIST_FILES=	bin/ftwin share/man/man8/ftwin.8.gz

OPTIONS_DEFINE=	DOCS

post-patch:
	@${REINPLACE_CMD} -e \
		's|-Werror -g -ggdb|| ; \
		 s|-O0||' ${WRKSRC}/Makefile.am

post-install-DOCS-on:
	@${MKDIR} ${STAGEDIR}${DOCSDIR}
	cd ${WRKSRC} && ${INSTALL_DATA} ${PORTDOCS} ${STAGEDIR}${DOCSDIR}

.include <bsd.port.mk>
