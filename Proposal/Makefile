DOCUMENT=Thesis\ Proposal.pdf
DELETE =  *.aux *.log *.ps *.dvi *.bbl *.blg *~ $(DOCUMENT) *.brf *.idx *.ilg *.ind *.lof *.lot *.out *.toc *.nlo *nls

# For Mac with texlive
PDFTEX=/usr/local/texlive/2009/bin/universal-darwin/pdflatex
MAKEINDEX=/usr/local/texlive/2009/bin/universal-darwin/makeindex 
MAKEINDEXSTYLE=/usr/local/texlive/2009//texmf-dist/makeindex/nomencl/nomencl.ist

all: $(DOCUMENT)

$(DOCUMENT): main.tex main.nls Body/*.tex
	@$(PDFTEX) main.tex
	@mv main.pdf $(DOCUMENT)

main.nls: main.nlo
	@$(MAKEINDEX) -s $(MAKEINDEXSTYLE) $< -o $@

main.nlo: main.tex Body/*.tex
	@$(PDFTEX) main.tex

clean:
	rm -f $(DELETE)
