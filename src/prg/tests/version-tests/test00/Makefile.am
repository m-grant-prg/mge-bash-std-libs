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


test00.sh: Makefile
	mkdir -p $(@D)
	rm -f $@ $@.tmp
	test -f ./$@.in || srcdir=$(srcdir)/; \
	$(edit) $${srcdir}$(@).in > $@.tmp
	mv $@.tmp $@
	chmod a+x $@
test00.sh: $(srcdir)/test00.sh.in


test00-stderr-answer.txt test00-stdout-answer.txt: Makefile
	mkdir -p $(@D)
	rm -f $@ $@.tmp
	test -f ./$@.in || srcdir=$(srcdir)/; \
	$(edit) $${srcdir}$(@).in > $@.tmp
	mv $@.tmp $@
test00-stderr-answer.txt: $(srcdir)/test00-stderr-answer.txt.in
test00-stdout-answer.txt: $(srcdir)/test00-stdout-answer.txt.in


check_DATA = test00.sh test00-stderr-answer.txt \
	     test00-stdout-answer.txt


EXTRA_DIST = $(srcdir)/test00.sh.in \
	     test00-stderr-answer.txt.in test00-stdout-answer.txt.in


CLEANFILES = *.tmp test00.sh test00-stderr-answer.txt \
	     test00-stdout-answer.txt test00-stderr-result.txt \
	     test00-stdout-result.txt

