PROJ=proj4

.PHONY: clean zip all

all: $(PROJ).pdf

$(PROJ).pdf: $(PROJ).ps
	ps2pdf -sPAPERSIZE=a4 $^

$(PROJ).ps: $(PROJ).dvi
	dvips $^

$(PROJ).dvi: $(PROJ).tex
	latex $^
	bibtex $(PROJ)
	latex $^
	latex $^

zip: all
	zip xzmitk01-fit.zip $(PROJ).tex czechiso.bst $(PROJ).bib Makefile

clean:
	rm -f $(PROJ).pdf $(PROJ).aux $(PROJ).dvi $(PROJ).log $(PROJ).ps $(PROJ).synctex.gz $(PROJ).fls $(PROJ).fdb_latexmk $(PROJ).bbl $(PROJ).blg
