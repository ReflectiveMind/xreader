AM_CPPFLAGS =					\
	-I$(top_srcdir)				\
	-I$(top_srcdir)/libdocument		\
	-DXREADER_LOCALE_DIR=\"$(datadir)/locale\"	\
	-DXREADER_COMPILATION			\
	$(BACKEND_CFLAGS)			\
	$(WARN_CFLAGS)				\
	$(DISABLE_DEPRECATED)

backend_LTLIBRARIES = libpixbufdocument.la

libpixbufdocument_la_SOURCES =		\
	pixbuf-document.c		\
	pixbuf-document.h

libpixbufdocument_la_LDFLAGS = $(BACKEND_LIBTOOL_FLAGS)
libpixbufdocument_la_LIBADD =				\
	$(top_builddir)/libdocument/libxreaderdocument.la	\
	$(BACKEND_LIBS)

backend_in_files = pixbufdocument.xreader-backend.in
backend_DATA = $(backend_in_files:.xreader-backend.in=.xreader-backend)

EXTRA_DIST = $(backend_in_files)

CLEANFILES = $(backend_DATA)

@EV_INTLTOOL_XREADER_BACKEND_RULE@

-include $(top_srcdir)/git.mk
