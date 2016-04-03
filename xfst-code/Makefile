# Makefile for xfst code
# Type "make dir-syll" to run code for direct syllable account
# Type "make ot-syll" to run code for OT syllable account
# Type "make dir-ft" to run code for direct fodir account
# Type "make ot-ft" to run code for OT foot account

SYLLDIRS = dir-syll ot-syll
FTDIRS = dir-ft ot-ft
.PHONY: subdirs $(SYLLDIRS)
.PHONY: subdirs $(FTDIRS)

dir-syll:
	$(MAKE) -C dir-syll all

ot-syll:
	$(MAKE) -C ot-syll all

dir-ft:
	$(MAKE) -C dir-ft all

ot-ft:
	$(MAKE) -C ot-ft all
