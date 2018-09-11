available=$(shell ls *rocm_[0-9]*.tsv |sed -e 's/_[0-9]\+.tsv//'|sort -u)

all: condense

list-datasets:
	@echo $(PWD) ":"
	@echo $(available)|sort|tr ' ' '\n'

%-condensed.tsv : #%-[0-9]*.tsv
	echo $@
	@sed -n '1p' $(@:%-condensed.tsv=%_1.tsv) > $@
	@for f in ${@:%-condensed.tsv=%_[0-9]*.tsv}; do echo processing $$f "->" $@; sed -n '2~1p' $$f >> $@;done

condense: $(available:%=%-condensed.tsv)


clean:
	rm -fv *-condensed.tsv
