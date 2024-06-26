PORTNAME=	mod_auth_openid
PORTVERSION=	0.8
DISTVERSIONPREFIX=	v
PORTREVISION=	2
CATEGORIES=	www
PKGNAMEPREFIX=	${APACHE_PKGNAMEPREFIX}

MAINTAINER=	joneum@FreeBSD.org
COMMENT=	Authentication module for the Apache 2 web server with OpenID
WWW=		https://findingscience.com/mod_auth_openid/

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/COPYING

DEPRECATED=	Depends on expired devel/libopkele
EXPIRATION_DATE=2024-05-24

LIB_DEPENDS=	libopkele.so:devel/libopkele \
		libsqlite3.so:databases/sqlite3

USES=		apache autoreconf cpe gmake libtool pkgconfig
USE_GITHUB=	yes
GH_ACCOUNT=	bmuller

PLIST_FILES=	${APACHEMODDIR}/mod_auth_openid.so
GNU_CONFIGURE=	yes
CONFIGURE_ARGS=	--with-pcre=${LOCALBASE}
CFLAGS+=	-I${LOCALBASE}/include -I/usr/include/openssl

CPE_VENDOR=	findingscience

post-patch:
	@${REINPLACE_CMD} -e 's|$${APXS} -i|$${APXS} -S LIBEXECDIR=${STAGEDIR}${PREFIX}/${APACHEMODDIR} -i|' \
		${WRKSRC}/src/Makefile.am

pre-install:
	@${MKDIR} ${STAGEDIR}${PREFIX}/${APACHEMODDIR}

post-install:
	${STRIP_CMD} ${STAGEDIR}${PREFIX}/${APACHEMODDIR}/${PORTNAME}.so

.include <bsd.port.mk>
