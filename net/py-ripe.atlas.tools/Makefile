PORTNAME=	ripe.atlas.tools
PORTVERSION=	2.3.0
PORTREVISION=	1
CATEGORIES=	net python
MASTER_SITES=	PYPI
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	mstucchi@ripe.net
COMMENT=	Official command-line client for RIPE Atlas
WWW=		https://github.com/RIPE-NCC/ripe-atlas-tools

LICENSE=	GPLv3
LICENSE_FILE=	${WRKSRC}/LICENSE

RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}python-dateutil>0:devel/py-python-dateutil@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}requests>=2.7.0:www/py-requests@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}ripe.atlas.cousteau>=1.0.4:net/py-ripe.atlas.cousteau@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}ripe.atlas.sagan>=1.1.4:net/py-ripe.atlas.sagan@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}tzlocal>0:devel/py-tzlocal@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}yaml>0:devel/py-yaml@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}openssl>=0.13:security/py-openssl@${PY_FLAVOR}

USES=		python
USE_PYTHON=	autoplist distutils
NO_ARCH=	yes

CONFLICTS_INSTALL=	c-ares # bin/adig

.include <bsd.port.mk>
