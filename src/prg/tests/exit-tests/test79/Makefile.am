#########################################################################
#									#
# Author: Copyright (C) 2026  Mark Grant				#
#									#
# Released under the GPLv3 only.					#
# SPDX-License-Identifier: GPL-3.0-only					#
#									#
# Purpose:								#
# AutoMake script file to generate mge-bash-std-libs tests.		#
#									#
#########################################################################


test79.sh test79a.sh: Makefile
	mkdir -p $(@D)
	rm -f $@ $@.tmp
	test -f ./$@.in || srcdir=$(srcdir)/; \
	$(edit) $${srcdir}$(@).in > $@.tmp
	mv $@.tmp $@
	chmod a+x $@
test79.sh: $(srcdir)/test79.sh.in
test79a.sh: $(srcdir)/test79a.sh.in


check_DATA = test79.sh test79a.sh


EXTRA_DIST = $(srcdir)/test79.sh.in $(srcdir)/test79a.sh.in


CLEANFILES = *.tmp test79.sh test79a.sh

