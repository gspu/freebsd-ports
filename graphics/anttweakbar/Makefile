PORTNAME=	anttweakbar
DISTVERSION=	1.16
PORTREVISION=	1
CATEGORIES=	graphics
MASTER_SITES=	SF/${PORTNAME}/
DISTNAME=	AntTweakBar_${DISTVERSION:S/.//}

MAINTAINER=	yuri@FreeBSD.org
COMMENT=	C library to add light and GUI into graphic apps
WWW=		https://anttweakbar.sourceforge.net/doc/

LICENSE=	ZLIB
LICENSE_FILE=	${WRKSRC}/../License.txt

USES=		dos2unix gl localbase:ldflags xorg zip
DOS2UNIX_FILES=	Makefile LoadOGLCore.h TwPrecomp.h
USE_GL=		gl glu
USE_LDCONFIG=	yes
USE_XORG=	x11

LDFLAGS+=	-lX11

BINARY_ALIAS=	gcc=${CC}

WRKSRC=		${WRKDIR}/AntTweakBar
WRKSRC_SUBDIR=	src

PLIST_FILES=	include/AntTweakBar.h \
		lib/libAntTweakBar.a \
		lib/libAntTweakBar.so \
		lib/libAntTweakBar.so.${DISTVERSION:R} \
		lib/libAntTweakBar.so.${DISTVERSION}

.include <bsd.port.options.mk>

post-patch:
.if ${OPSYS} == FreeBSD
	@${REINPLACE_CMD} -e 's|public binary_function|public __binary_function|' \
		${WRKSRC}/TwMgr.cpp
.endif

do-install:
	${INSTALL_DATA} ${WRKSRC}/../include/AntTweakBar.h ${STAGEDIR}${PREFIX}/include
	${INSTALL_DATA} ${WRKSRC}/../lib/libAntTweakBar.a ${STAGEDIR}${PREFIX}/lib
	${INSTALL_LIB} ${WRKSRC}/../lib/libAntTweakBar.so ${STAGEDIR}${PREFIX}/lib/libAntTweakBar.so.${DISTVERSION}
	cd ${STAGEDIR}${PREFIX}/lib && \
		${LN} -s libAntTweakBar.so.${DISTVERSION} libAntTweakBar.so.${DISTVERSION:R} && \
		${LN} -s libAntTweakBar.so.${DISTVERSION} libAntTweakBar.so

.include <bsd.port.mk>
