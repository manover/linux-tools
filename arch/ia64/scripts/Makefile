SCRIPTS = \
	check-gas \
	pvcheck.sed \
	toolchain-flags \
	unwcheck.py

DATA = \
	check-gas-asm.S \
	check-model.c \
	check-segrel.S \
	check-segrel.lds \
	check-serialize.S \
	check-text-align.S

OUTDIR = arch/ia64/scripts

top_srcdir = ../../..

VPATH = $(top_srcdir)/kbuild/$(OUTDIR)

# kluge for scripts added in Debian diff
$(top_srcdir)/kbuild/$(OUTDIR)/%: $(top_srcdir)/$(OUTDIR)/%
	mkdir -p $(@D)
	cp $< $@

include $(top_srcdir)/Makefile.inc
