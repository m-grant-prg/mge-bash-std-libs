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


test-02-11.sh: Makefile
	mkdir -p $(@D)
	rm -f $@ $@.tmp
	test -f ./$@.in || srcdir=$(srcdir)/; \
	$(edit) $${srcdir}$(@).in > $@.tmp
	mv $@.tmp $@
	chmod a+x $@
test-02-11.sh: $(srcdir)/test-02-11.sh.in


test-02-11-stderr-answer.txt test-02-11-stdout-answer.txt: Makefile
	mkdir -p $(@D)
	rm -f $@ $@.tmp
	test -f ./$@.in || srcdir=$(srcdir)/; \
	cp $${srcdir}$(@F).in  $@
test-02-11-stderr-answer.txt: $(srcdir)/test-02-11-stderr-answer.txt.in
test-02-11-stdout-answer.txt: $(srcdir)/test-02-11-stdout-answer.txt.in


check_DATA = test-02-11.sh test-02-11-stderr-answer.txt \
	     test-02-11-stdout-answer.txt


EXTRA_DIST = $(srcdir)/test-02-11.sh.in \
	     test-02-11-stderr-answer.txt.in test-02-11-stdout-answer.txt.in


CLEANFILES = *.tmp test-02-11.sh test-02-11-stderr-answer.txt \
	     test-02-11-stdout-answer.txt test-02-11-stderr-result.txt \
	     test-02-11-stdout-result.txt

