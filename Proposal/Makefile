DOCUMENT=Thesis\ Proposal.pdf
DELETE =  *.aux *.log *.ps *.dvi *.bbl *.blg *~ $(DOCUMENT) *.brf *.idx *.ilg *.ind *.lof *.lot *.out *.toc *.nlo *nls

# For Mac with texlive
PDFTEX=/usr/local/texlive/2009/bin/universal-darwin/pdflatex
BIBTEX=/usr/local/texlive/2009/bin/universal-darwin/bibtex

all: $(DOCUMENT)

$(DOCUMENT): main.tex main.bbl Body/*.tex
	$(PDFTEX) main.tex
	mv main.pdf $(DOCUMENT)

main.bbl: main.aux
	$(BIBTEX) $<

main.aux: main.tex Body/*.tex
	$(PDFTEX) main.tex

clean:
	rm -f $(DELETE)
