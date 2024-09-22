UNAME := $(shell uname)
LATEX = pdflatex
DOC = main
IMGDIR = pics
SUBDIRS = $(IMGDIR)
OPEN = open

ifeq ($(UNAME), Linux)
	LATEX=pdflatex 
	OPEN = xdg-open
endif

.PHONY: clean $(SUBDIRS)

all: build

me: build
	$(OPEN) $(DOC).pdf &

build:
	$(LATEX) --shell-escape $(DOC).tex
	-bibtex $(DOC).aux || echo "OK" && \
	  $(LATEX) --shell-escape $(DOC).tex && \
	  $(LATEX) --shell-escape $(DOC).tex

clean: $(SUBDIRS)
	rm -f $(DOC).pdf *.ps *.aux *.bbl *.blg *.dvi *.log *.toc *.fls *.fdb_latexmk *.synctex.gz *.out *.ent
	rm -rf _minted-main/


#    $(SUBDIRS):
#	$(MAKE) -C $(SUBDIRS) clean
