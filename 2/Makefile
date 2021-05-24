target=proj2
login=xzmitk01

all: $(target).pdf

$(target).pdf:
	pdflatex $(target).tex
	pdflatex $(target).tex

zip:
	zip $(login)-fit.zip $(target).tex Makefile

clean:
	rm -f  $(target).aux  $(target).out $(target).log $(target).pdf $(login)-fit.zip

.PHONY: all clean zip
