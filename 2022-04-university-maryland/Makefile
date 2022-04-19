BIBTEX = bibtex
MAIN = naval-postgrad-seminar

all: $(MAIN).pdf

$(MAIN).pdf: $(MAIN).tex
	while $(LATEX) $(MAIN) && grep -q "Rerun to get" $(MAIN).log ; do true; done

$(MAIN).bbl: $(MAIN).bib
	$(LATEX) $(MAIN)
	$(BIBTEX) $(MAIN)

clean:
	rm -f *.bbl *.blg main.pdf *.aux *.log *.out *.nav *.toc *.snm *.pdf *.pdfpc

