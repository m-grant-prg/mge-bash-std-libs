#########################################################################
#									#
# Author: Copyright (C) 2026  Mark Grant				#
#									#
# Released under the GPLv3 only.					#
# SPDX-License-Identifier: GPL-3.0-only					#
#									#
# Purpose:								#
# AutoMake script file to generate mge bash standard libraries.		#
#									#
#########################################################################


mge-basic-lib.sh mge-script-exit-lib.sh: Makefile
	mkdir -p $(@D)
	rm -f $@ $@.tmp
	test -f ./$@.in || srcdir=$(srcdir)/; \
	$(edit) $${srcdir}$(@F).in > $@.tmp
	mv $@.tmp $@
mge-basic-lib.sh: $(srcdir)/mge-basic-lib.sh.in
mge-script-exit-lib.sh: $(srcdir)/mge-script-exit-lib.sh.in


pkgdata_DATA = mge-basic-lib.sh mge-script-exit-lib.sh


EXTRA_DIST = $(srcdir)/mge-basic-lib.sh.in mge-script-exit-lib.sh.in

CLEANFILES = *.tmp mge-basic-lib.sh mge-script-exit-lib.sh
