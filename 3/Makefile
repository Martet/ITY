target=proj3
login=xzmitk01

all: $(target).pdf

$(target).pdf: $(target).ps
	ps2pdf -sPAPERSIZE=a4 $(target).ps

$(target).ps: $(target).dvi
	dvips $(target).dvi

$(target).dvi:
	latex $(target).tex
	latex $(target).tex

zip:
	zip $(login)-fit.zip *.tex *.eps *.sty Makefile

clean:
	rm -f  *.log $(target).aux  $(target).out $(target).log $(target).pdf $(target).ps $(target).dvi $(login)-fit.zip

.PHONY: all clean zip
