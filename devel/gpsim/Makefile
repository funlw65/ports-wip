# $OpenBSD:$

COMMENT =		PIC microcontroller emulator
DISTNAME =		gpsim-0.30.0
PKGNAME =		gpsim-0.30.0

CATEGORIES =		devel

HOMEPAGE =		http://gpsim.sourceforge.net

MAINTAINER =		Ralf Horstmann <ralf-lists@ackstorm.de>

# GPLv2+ LGPLv2+
PERMIT_PACKAGE_CDROM =	Yes

SHARED_LIBS +=  gpsim                     0.0 # 0.0
SHARED_LIBS +=  gpsim_dspic               0.0 # 0.0
SHARED_LIBS +=  gpsim_eXdbm               0.0 # 0.0
SHARED_LIBS +=  gpsim_modules             0.0 # 0.0
SHARED_LIBS +=  gpsimcli                  0.0 # 0.0
SHARED_LIBS +=  gpsimgui                  0.0 # 0.0
SHARED_LIBS +=  gpsim_extras              0.0 # 0.0

WANTLIB = c m readline z
WANTLIB += X11 Xcomposite Xcursor Xdamage Xext Xfixes Xi Xinerama
WANTLIB += Xrandr Xrender atk-1.0 cairo expat ffi fontconfig freetype
WANTLIB += gdk-x11-2.0 gtk-x11-2.0 iconv
WANTLIB += intl pcre pixman-1 png popt pthread
WANTLIB += xcb xcb-render xcb-shm gmodule-2.0 graphite2
WANTLIB += gdk_pixbuf-2.0 gio-2.0 glib-2.0 gobject-2.0 gthread-2.0
WANTLIB += pango-1.0 pangocairo-1.0 pangoft2-1.0 harfbuzz
WANTLIB += ${COMPILER_LIBCXX} curses fribidi

MASTER_SITES =		${MASTER_SITE_SOURCEFORGE:=gpsim/}

BUILD_DEPENDS =		devel/libtool

LIB_DEPENDS =		x11/gtk+2 \
			devel/popt

CONFIGURE_STYLE =	gnu
CONFIGURE_ENV =		CPPFLAGS="-I${LOCALBASE}/include" CFLAGS="-L${LOCALBASE}/lib"
USE_LIBTOOL=		gnu

AUTOCONF_VERSION =	2.69
AUTOMAKE_VERSION =	1.11

post-install:
	rm ${PREFIX}/lib/libgpsim*.la
	rm ${PREFIX}/lib/libgpsim*.a

.include <bsd.port.mk>
