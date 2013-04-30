PORTNAME=		nmsg
PORTVERSION=	0.7.3
CATEGORIES=		net
MASTER_SITES=	http://rsfcode.isc.org/dist/nmsg/

MAINTAINER=		edmonds@isc.org
COMMENT=		network message encapsulation system

LIB_DEPENDS=	pcap.1:${PORTSDIR}/net/libpcap

BUILD_DEPENDS=	\
	${LOCALBASE}/libdata/pkgconfig/libprotobuf-c.pc:${PORTSDIR}/devel/protobuf-c \
	${LOCALBASE}/libdata/pkgconfig/libwdns.pc:${PWD}/../wdns \
	${LOCALBASE}/libdata/pkgconfig/libxs.pc:${PWD}/../libxs

USE_GMAKE=	yes
USE_PKGCONFIG=	yes

GNU_CONFIGURE=	yes
CONFIGURE_ARGS+=	--with-pkgconfigdir='$${exec_prefix}/libdata/pkgconfig' CFLAGS="-I/usr/local/include" LDFLAGS="-L/usr/local/lib"

.include <bsd.port.mk>
