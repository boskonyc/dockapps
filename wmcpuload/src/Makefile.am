bin_PROGRAMS = wmcpuload

wmcpuload_SOURCES = \
	cpu.h \
	cpu_@OS@.c \
	main.c \
	backlight_on.xpm \
	backlight_off.xpm \
	parts.xpm

EXTRA_wmcpuload_SOURCES = \
	cpu_linux.c \
	cpu_freebsd.c \
	cpu_openbsd.c \
	cpu_netbsd.c \
	cpu_bsdi.c \
	cpu_solaris.c \
	cpu_cygwin.c

wmcpuload_DEPENDENCIES = ../libdockapp/dockapp.o

INCLUDES = \
	@HEADER_SEARCH_PATH@ \
	@XCFLAGS@

CFLAGS = @DFLAGS@ @CFLAGS@ -I../libdockapp/

wmcpuload_LDADD = \
	dockapp.o \
	@LIBRARY_SEARCH_PATH@ \
	@XLIBS@ \
	@XLFLAGS@

INSTALL_PROGRAM = \
	@INSTALL_PROGRAM@ \
	@SETGID_FLAGS@ \
	$(AM_INSTALL_PROGRAM_FLAGS)
