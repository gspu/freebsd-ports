PORTREVISION=	2	# don't delete, reset to 0
CATEGORIES=	net
PKGNAMESUFFIX=	-libdns

MAINTAINER=	desktop@FreeBSD.org
COMMENT=	mDNSResponder compatibility from Avahi

LIB_DEPENDS=	libavahi-common.so:net/avahi-app

MASTERDIR=	${.CURDIR}/../avahi-app
BUILD_WRKSRC=	${WRKSRC}/avahi-compat-libdns_sd
INSTALL_WRKSRC=	${BUILD_WRKSRC}
DESCR=		${.CURDIR}/pkg-descr
PLIST=		${.CURDIR}/pkg-plist

AVAHI_SLAVE=	libdns
AVAHI_PKGCONFIG=avahi-compat-libdns_sd.pc

CONFLICTS=	mDNSResponder

.include "${MASTERDIR}/Makefile"
