PORTNAME=	gaffitter
PORTVERSION=	0.6.0
PORTREVISION=	2
CATEGORIES=	sysutils
MASTER_SITES=	SF

MAINTAINER=	ports@FreeBSD.org
COMMENT=	Binary packing utility that uses a genetic algorithm
WWW=		https://gaffitter.sourceforge.net/

LICENSE=	GPLv3+
LICENSE_FILE=	${WRKSRC}/COPYING

USES=		gmake tar:bzip2	# parallel builds (-jX) are broken with BSD make(1)

PLIST_FILES=	bin/${PORTNAME} share/man/man1/${PORTNAME}.1.gz

# Change "cd foo; $(MAKE)" into "$(MAKE) -C foo" to unbreak parallel builds
post-patch:
	@${REINPLACE_CMD} -E 's|cd (.+); (\$$\(MAKE\))|\2 -C \1|' \
		${WRKSRC}/Makefile
	@${REINPLACE_CMD} -e 's|g++|${CXX}|g' ${WRKSRC}/src/Makefile

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/src/${PORTNAME} ${STAGEDIR}${PREFIX}/bin
	${INSTALL_MAN} ${FILESDIR}/${PORTNAME}.1 ${STAGEDIR}${PREFIX}/share/man/man1

.include <bsd.port.mk>
