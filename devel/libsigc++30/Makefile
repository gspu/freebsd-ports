PORTNAME=	libsigc++
PORTVERSION=	3.6.0
CATEGORIES=	devel
MASTER_SITES=	GNOME
PKGNAMESUFFIX=	30

MAINTAINER=	gnome@FreeBSD.org
COMMENT=	Callback Framework for C++
WWW=		https://libsigcplusplus.github.io/libsigcplusplus/index.html

LICENSE=	LGPL21+
LICENSE_FILE=	${WRKSRC}/COPYING

USES=		compiler:c++17-lang gnome meson pkgconfig python:build tar:xz
USE_GNOME=	libxslt:build
USE_LDCONFIG=	yes

MESON_ARGS=	-Dbuild-documentation=false \
		-Dbuild-examples=false

PLIST_SUB=	API_VERSION="3.0"

.include <bsd.port.mk>
