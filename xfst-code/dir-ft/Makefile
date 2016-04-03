# pathname to gold standard for correct outputs
GOLDFT="../auxiliary/gold-output5-footed.txt"


all:
	@echo +++ Sort gold standard correct list of 47 outputs +++
	sort $(GOLDFT) > tmp-gold

	@echo +++ Define grammar in xfst and generate outputs for testing over/undergeneration +++
	xfst -f grammar.xfst

	@echo +++ For generated output of grammar for {L,H}* inputs up to 5 syllables +++
	@echo +++ check against correct set of outputs for inputs up to 5 syll +++
	@echo +++ Check if any overgeneration compared to gold standard +++
	sort < chk-overgen.txt | sed '1d' | diff tmp-gold - || echo 'Files differ'
	@echo +++ Check number of output strings from chk-overgen.txt +++
	sed '1d' chk-overgen.txt | wc -l

	@echo +++ From intersecting output of grammar with correct set of outputs for inputs up to 5 syll +++
	@echo +++ Check against correct set of outputs for inputs up to 5 syll +++
	sort < chk-undergen.txt | sed '1d' | diff tmp-gold - || echo 'Files differ'
	@echo +++ Check number of output strings from chk-undergen.txt +++
	sed '1d' chk-undergen.txt | wc -l

	rm -f tmp-gold

