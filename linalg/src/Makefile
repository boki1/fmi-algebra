OUTDIR=out
INDIR=.

all:
	mkdir -p $(OUTDIR)
	pdflatex -output-directory=$(OUTDIR) main.tex
	makeglossaries -d $(OUTDIR) main
	pdflatex -output-directory=$(OUTDIR) main.tex
	biber --output-directory=$(OUTDIR) main
	pdflatex -output-directory=$(OUTDIR) main.tex
	ln -sf $(OUTDIR)/main.pdf ./main.pdf

clean:
	rm -rf $(OUTDIR) main.pdf

.PHONY: all clean
