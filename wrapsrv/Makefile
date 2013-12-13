PORTNAME=	wrapsrv
PORTVERSION=	0.3
CATEGORIES=	dns
MASTER_SITES=	https://dl.farsightsecurity.com/dist/wrapsrv/

MAINTAINER=	software@farsightsecurity.com
COMMENT=	DNS SRV record command line wrapper

post-patch:
	@${REINPLACE_CMD} -e 's/^LDFLAGS = -lresolv$$/LDFLAGS = /g' ${WRKSRC}/Makefile

.include <bsd.port.mk>
