templatetestsdir = $(prefix)/share/fw/template/@FW_TEMPLATE_TEMPLATE_TYPE@/tests

dist_templatetests_SCRIPTS =		\
  test-wrapper.sh.in

noinst_DATA =				\
  $(dist_templatetests_SCRIPTS:%=.%.script_ok)

dist_templatetests_DATA =               \
  Makefile_dot_am			\
  Makefile.am.local			\
  testprog.c

install-data-hook:
	find "$(DESTDIR)$(templatetestsdir)" -type f | xargs chmod -w

CLEANFILES =

MAINTAINERCLEANFILES = 			\
  Makefile.in

include $(top_srcdir)/fw/build/automake/check-shell.am
include $(top_srcdir)/fw/build/automake/gnu-make-check.am
