PORTNAME=	nmsg
REALVERSION=	0.8.0-rc2
PORTVERSION=	0.8.0.rc2
DISTNAME=	${PORTNAME}-${REALVERSION}
CATEGORIES=	net
MASTER_SITES=	https://dl.farsightsecurity.com/dist/nmsg/test/${REALVERSION}/
MAINTAINER=	software@farsightsecurity.com
COMMENT=	network message encapsulation system

BUILD_DEPENDS=	\
	${LOCALBASE}/libdata/pkgconfig/libprotobuf-c.pc:${PORTSDIR}/devel/protobuf-c \
	${LOCALBASE}/libdata/pkgconfig/libwdns.pc:${PWD}/../wdns

USE_PKGCONFIG=	yes
GNU_CONFIGURE=	yes
USES=		pathfix gmake
CFLAGS+=	"-I/usr/local/include"
LDFLAGS+=	"-L/usr/local/lib"
CONFIGURE_ARGS+=	--without-libxs
CONFIGURE_ARGS+=	--with-pkgconfigdir='$${exec_prefix}/libdata/pkgconfig'

.include <bsd.port.mk>
