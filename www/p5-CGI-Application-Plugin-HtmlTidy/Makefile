PORTNAME=	CGI-Application-Plugin-HtmlTidy
PORTVERSION=	1.05
PORTREVISION=	1
CATEGORIES=	www perl5
MASTER_SITES=	CPAN
PKGNAMEPREFIX=	p5-

MAINTAINER=	bofh@FreeBSD.org
COMMENT=	Add HTML::Tidy support to CGI::Application
WWW=		https://metacpan.org/release/CGI-Application-Plugin-HtmlTidy

LICENSE=	ART10 GPLv1+
LICENSE_COMB=	dual

DEPRECATED=	Depends on expired textproc/p5-HTML-Tidy
EXPIRATION_DATE=2025-02-01

BUILD_DEPENDS=	${RUN_DEPENDS}
RUN_DEPENDS=	p5-CGI-Application>4.01:www/p5-CGI-Application \
		p5-CGI-Application-Plugin-DevPopup>=0:www/p5-CGI-Application-Plugin-DevPopup \
		p5-HTML-Tidy>=1.08:textproc/p5-HTML-Tidy

USES=		perl5
USE_PERL5=	configure

.include <bsd.port.mk>
