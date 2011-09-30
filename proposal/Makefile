MAIN= paper
TEXPARTS= *.tex
BIBPARTS= *.bib
FIGPARTS= FIG

$(MAIN).pdf: $(MAIN).dvi
	dvipdf $(MAIN).dvi


$(MAIN).dvi: $(MAIN).tex
	latex $(MAIN).tex
	bibtex $(MAIN)
	latex $(MAIN).tex
	latex $(MAIN).tex

clean:
	\rm -f *.dvi *.bbl *.aux *.log *.blg *.toc

spotless: clean
	\rm -f $(MAIN).ps


all.tar:
	tar cvfh all.tar makefile $(MAIN).tex $(TEXPARTS) $(BIBPARTS) \
	$(FIGPARTS) README psfig.sty

