PORTNAME=	libkcompactdisc
DISTVERSION=	${KDE_APPLICATIONS_VERSION}
CATEGORIES=	audio kde kde-applications

MAINTAINER=	kde@FreeBSD.org
COMMENT=	KDE library for interfacing with audio CDs
WWW=		https://www.kde.org/

USES=		cmake compiler:c++11-lang gettext kde:5 qt:5 tar:xz
USE_KDE=	coreaddons emoticons i18n itemmodels itemviews \
		kdelibs4support phonon solid \
		ecm:build
USE_QT=		core dbus gui widgets \
		buildtools:build qmake:build
USE_LDCONFIG=	yes

OPTIONS_DEFINE=	ALSA DOCS

ALSA_LIB_DEPENDS=	libasound.so:audio/alsa-lib
ALSA_CMAKE_BOOL_OFF=	CMAKE_DISABLE_FIND_PACKAGE_ALSA

.include <bsd.port.mk>
