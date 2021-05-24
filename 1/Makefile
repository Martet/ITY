HELL = /usr/bin/env bash
NAME = proj1
LOGIN = xzmitk01

all:
	pdflatex $(NAME).tex

zip:
	zip $(LOGIN)-fit.zip *.tex Makefile

clean:
	rm -f $(NAME).{aux,dvi,log,pdf,ps,out} $(LOGIN)-fit.zip
