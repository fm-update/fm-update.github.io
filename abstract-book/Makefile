MAIN = main
LATEX = pdflatex
LATEXOPTS = -interaction=nonstopmode -halt-on-error

.PHONY: all clean distclean

all: $(MAIN).pdf

$(MAIN).pdf: $(MAIN).tex dagrep.cls
	$(LATEX) $(LATEXOPTS) $(MAIN).tex
	$(LATEX) $(LATEXOPTS) $(MAIN).tex
	$(LATEX) $(LATEXOPTS) $(MAIN).tex

dagrep.cls:
	@echo "ERROR: dagrep.cls is missing."
	@echo "Download the Dagstuhl author kit from https://submission.dagstuhl.de/documentation/authors"
	@echo "and place dagrep.cls (plus dagrep-logo.pdf and any auxiliary files) in this directory."
	@exit 1

clean:
	rm -f $(MAIN).aux $(MAIN).log $(MAIN).out $(MAIN).toc $(MAIN).bbl $(MAIN).blg

distclean: clean
	rm -f $(MAIN).pdf
