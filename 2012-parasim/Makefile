TO_CLEAN=aux nav log blg bib~ sty~ bbl tex~ out toc snm idx dvi txt~ idx out blg
TO_MOVE=pdf

.PHONY: all
all: pdf clean

.PHONY: pdf
pdf: 
	pdflatex project; \
    bibtex project; \
	pdflatex project; \
	pdflatex project; \

.PHONY: clean
clean:
	@for EXT in $(TO_CLEAN); do \
		echo "--- DELETING *.$$EXT"; \
		for FILE in *.$$EXT; do \
			rm -f "$$FILE"; \
		done \
	done

