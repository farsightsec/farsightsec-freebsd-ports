PORTNAME=		libxs
PORTVERSION=		1.2.0
CATEGORIES=		net
MASTER_SITES=		http://download.crossroads.io/

MAINTAINER=		edmonds@isc.org
COMMENT=		Crossroads I/O lightweight messaging layer

USE_GMAKE=		yes
USE_PKGCONFIG=		yes

GNU_CONFIGURE=		yes

post-patch:
	${REINPLACE_CMD} -e 's|pkgconfigdir = $$(libdir)/pkgconfig|pkgconfigdir = $${exec_prefix}/libdata/pkgconfig|g' ${WRKSRC}/src/Makefile.in

.include <bsd.port.mk>
