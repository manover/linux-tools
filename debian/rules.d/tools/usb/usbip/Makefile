srcdir := $(top_srcdir)/tools/usb/usbip

# Make sure we don't override top_srcdir in the sub-make.  'unexport
# top_srcdir' is *not* sufficient; nor is adding 'MAKEFLAGS=' to the
# sub-make command line.
unexport MAKEFLAGS

all:
	cd $(srcdir) && ./autogen.sh
	$(shell dpkg-buildflags --export=cmdline) $(srcdir)/configure \
		--prefix=/usr \
		--with-tcp-wrappers \
		--with-usbids-dir=/usr/share/misc \
		--disable-shared
	$(MAKE)

install:
	$(MAKE) install

clean:
	rm -rf $(addprefix $(srcdir)/,autom4te.cache aclocal.m4 compile config.guess config.h.in config.sub configure depcomp install-sh ltmain.sh missing)
	find $(srcdir)/ -name Makefile.in -delete
