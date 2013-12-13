PORTNAME=	sie-nmsg
PORTVERSION=	0.14
CATEGORIES=	net
MASTER_SITES=	https://dl.farsightsecurity.com/dist/sie-nmsg/

MAINTAINER=	software@farsightsecurity.com
COMMENT=	SIE message module plugin for libnmsg

BUILD_DEPENDS=  \
	${LOCALBASE}/libdata/pkgconfig/libprotobuf-c.pc:${PORTSDIR}/devel/protobuf-c \
	${LOCALBASE}/libdata/pkgconfig/libnmsg.pc:${PWD}/../nmsg \
	${LOCALBASE}/libdata/pkgconfig/libwdns.pc:${PWD}/../wdns

USE_GMAKE=		yes
USE_PKGCONFIG=		yes

GNU_CONFIGURE=		yes
CONFIGURE_ARGS+=	CFLAGS="-I/usr/local/include" LDFLAGS="-L/usr/local/lib"

.include <bsd.port.mk>
