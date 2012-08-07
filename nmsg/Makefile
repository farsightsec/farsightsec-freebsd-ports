PORTNAME=		nmsg
PORTVERSION=	0.7.1
CATEGORIES=		net
MASTER_SITES=	http://rsfcode.isc.org/dist/nmsg/

MAINTAINER=		edmonds@isc.org
COMMENT=		network message encapsulation system

LIB_DEPENDS=	pcap.1:${PORTSDIR}/net/libpcap

BUILD_DEPENDS=	\
	${LOCALBASE}/libdata/pkgconfig/libprotobuf-c.pc:${PORTSDIR}/devel/protobuf-c \
	${LOCALBASE}/libdata/pkgconfig/libwdns.pc:${PWD}/../wdns

USE_GMAKE=	yes
USE_PKGCONFIG=	yes

GNU_CONFIGURE=	yes
CONFIGURE_ARGS+=	CFLAGS="-I/usr/local/include" LDFLAGS="-L/usr/local/lib"

post-patch:
	${REINPLACE_CMD} -e 's|pkgconfigdir = $$(libdir)/pkgconfig|pkgconfigdir = $${exec_prefix}/libdata/pkgconfig|g' ${WRKSRC}/Makefile.in

.include <bsd.port.mk>
