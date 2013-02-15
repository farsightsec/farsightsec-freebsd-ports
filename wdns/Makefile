PORTNAME=		wdns
PORTVERSION=	0.4
CATEGORIES=		net
MASTER_SITES=	http://rsfcode.isc.org/dist/wdns/

MAINTAINER=		edmonds@isc.org
COMMENT=		low-level DNS library

LIB_DEPENDS=	pcap.1:${PORTSDIR}/net/libpcap

USE_GMAKE=		yes
USE_PKGCONFIG=	yes

GNU_CONFIGURE=	yes
CONFIGURE_ARGS+=	CFLAGS="-I/usr/local/include" LDFLAGS="-L/usr/local/lib"

post-patch:
	${REINPLACE_CMD} -e 's|pkgconfigdir = $$(libdir)/pkgconfig|pkgconfigdir = $${exec_prefix}/libdata/pkgconfig|g' ${WRKSRC}/Makefile.in

.include <bsd.port.mk>
