libyami_common_source_c = \
	log.cpp \
	utils.cpp \
	nalreader.cpp \
	surfacepool.cpp \
	PooledFrameAllocator.cpp \
	YamiVersion.cpp \
	$(NULL)

libyami_common_source_h = \
	YamiVersion.h \
	$(NULL)

libyami_common_source_h_priv = \
	Array.h \
	NonCopyable.h \
	Functional.h \
	log.h \
	utils.h \
	common_def.h \
	nalreader.h \
	videopool.h \
	surfacepool.h \
	$(NULL)

libyami_common_ldflags = \
	$(LIBYAMI_LT_LDFLAGS) \
	$(LIBVA_LIBS) \
	$(LIBVA_DRM_LIBS) \
	$(NULL)

#to compile within yocto
extra_includes = \
        -I$(top_srcdir) \
        $(NULL)

libyami_common_cppflags = \
	$(LIBVA_CFLAGS) \
	-I$(top_srcdir)/interface \
	$(extra_includes) \
	$(NULL)

noinst_LTLIBRARIES            = libyami_common.la
libyami_commonincludedir      = ${includedir}/libyami
libyami_commoninclude_HEADERS = $(libyami_common_source_h)
libyami_common_la_SOURCES     = $(libyami_common_source_c)
libyami_common_la_LDFLAGS     = $(libyami_common_ldflags) $(AM_LDFLAGS)
libyami_common_la_CPPFLAGS    = $(libyami_common_cppflags) $(AM_CPPFLAGS)

if ENABLE_UNITTESTS
include Makefile.unittest
endif

DISTCLEANFILES = \
	Makefile.in\
	YamiVersion.h \
	$(NULL)


