PORTNAME=		nmsg
PORTVERSION=	0.6.17
CATEGORIES=		net
MASTER_SITES=	ftp://ftp.isc.org/isc/nmsg/

MAINTAINER=		edmonds@isc.org
COMMENT=		network message encapsulation system

LIB_DEPENDS=	pcap.1:${PORTSDIR}/net/libpcap

GNU_CONFIGURE=	yes
CONFIGURE_ARGS+=	CFLAGS="-I/usr/local/include" LDFLAGS="-L/usr/local/lib"

.include <bsd.port.mk>
