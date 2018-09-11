
SRC_FILES=$(wildcard *Rmd)

PDF_FILES=$(SRC_FILES:%.Rmd=%.pdf)
HTML_FILES=$(SRC_FILES:%.Rmd=%.html)

pdf : $(PDF_FILES)

html : $(HTML_FILES)

all : $(PDF_FILES) $(HTML_FILES)

%.html : %.Rmd
		Rscript -e "rmarkdown::render('$<')"

%.pdf : %.Rmd
		Rscript -e "rmarkdown::render('$<','pdf_document')"


clean :
		rm -fv $(PDF_FILES) $(HTML_FILES)
