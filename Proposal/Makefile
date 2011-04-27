DOCUMENT=Thesis\ Proposal.pdf
DELETE =  *.aux *.log *.ps *.dvi *.bbl *.blg *~ $(DOCUMENT) *.brf *.idx *.ilg *.ind *.lof *.lot *.out *.toc *.nlo *nls

all: $(DOCUMENT)

$(DOCUMENT): main.tex main.bbl Body/*.tex
	pdflatex main.tex
	mv main.pdf $(DOCUMENT)

main.bbl: main.aux
	bibtex $<

main.aux: main.tex Body/*.tex
	pdflatex main.tex

clean:
	rm -f $(DELETE)
