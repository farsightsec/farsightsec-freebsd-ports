PORTNAME=		wrapsrv
PORTVERSION=	0.2
CATEGORIES=		dns
MASTER_SITES=	http://rsfcode.isc.org/dist/wrapsrv/

MAINTAINER=		edmonds@isc.org
COMMENT=		DNS SRV record command line wrapper

post-patch:
	@${REINPLACE_CMD} -e 's/^LDFLAGS = -lresolv$$/LDFLAGS = /g' ${WRKSRC}/Makefile

.include <bsd.port.mk>
