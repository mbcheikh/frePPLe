#
# Process this file with automake to produce Makefile.in
#

sources = lpsolver.cpp lpsolver.h

EXTRA_DIST = $(sources) mod_lpsolver.xsd

if LP

pkglib_LTLIBRARIES = mod_lpsolver.la
mod_lpsolver_la_SOURCES = $(sources)
mod_lpsolverdir = $(datadir)/frepple
mod_lpsolver_DATA = mod_lpsolver.xsd
mod_lpsolver_la_LDFLAGS = -module -shrext .so -avoid-version
mod_lpsolver_la_LIBADD = ../../src/libfrepple.la -lglpk

if CYGWIN
# Cygwin doesn't like undefined symbols in a windows dll
mod_lpsolver_la_LDFLAGS += -no-undefined
endif

# A convenience copy to quickly collect the results
all-local:
	-cp .libs/mod_lpsolver.so ../../bin
	cp mod_lpsolver.xsd ../../bin

endif

CLEANFILES = *.gcda *.gcov *.gcno
