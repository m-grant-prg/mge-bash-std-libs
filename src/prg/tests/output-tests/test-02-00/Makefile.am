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


test-02-00.sh: Makefile
	mkdir -p $(@D)
	rm -f $@ $@.tmp
	test -f ./$@.in || srcdir=$(srcdir)/; \
	$(edit) $${srcdir}$(@).in > $@.tmp
	mv $@.tmp $@
	chmod a+x $@
test-02-00.sh: $(srcdir)/test-02-00.sh.in


test-02-00-stderr-answer.txt test-02-00-a-stderr-answer.txt \
	test-02-00-stdout-answer.txt test-02-00-a-stdout-answer.txt: Makefile
	mkdir -p $(@D)
	rm -f $@ $@.tmp
	test -f ./$@.in || srcdir=$(srcdir)/; \
	cp $${srcdir}$(@F).in  $@
test-02-00-stderr-answer.txt: $(srcdir)/test-02-00-stderr-answer.txt.in
test-02-00-a-stderr-answer.txt: $(srcdir)/test-02-00-a-stderr-answer.txt.in
test-02-00-stdout-answer.txt: $(srcdir)/test-02-00-stdout-answer.txt.in
test-02-00-a-stdout-answer.txt: $(srcdir)/test-02-00-a-stdout-answer.txt.in


check_DATA = test-02-00.sh test-02-00-stderr-answer.txt \
	     test-02-00-a-stderr-answer.txt test-02-00-stdout-answer.txt \
	     test-02-00-a-stdout-answer.txt


EXTRA_DIST = $(srcdir)/test-02-00.sh.in test-02-00-stderr-answer.txt.in \
	     $(srcdir)/test-02-00-a-stderr-answer.txt.in \
	     test-02-00-stdout-answer.txt.in \
	     $(srcdir)/test-02-00-a-stdout-answer.txt.in


CLEANFILES = *.tmp test-02-00.sh test-02-00-stderr-answer.txt \
	     test-02-00-a-stderr-answer.txt test-02-00-stdout-answer.txt \
	     test-02-00-stderr-result.txt test-02-00-stdout-result.txt \
	     test-02-00-a-stdout-answer.txt

