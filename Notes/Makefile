# .PHONY: main clean FORCE main.pdf

# main: main.pdf

# main.bbl: main.pdf bibtex main.aux

# main.pdf: FORCE
# 	pdflatex -synctex=1 -interaction=nonstopmode main.tex

# clean:
# 	rm main.bbl main.blg main.aux

# main: main.pdf

# main.pdf: main.tex
# 	pdflatex -synctex=1 -interaction=nonstopmode main.tex
# 	bibtex main.aux

# clean:
# 	rm main.bbl main.blg main.aux


.PHONY: all clean
all: main.pdf

main.pdf: main.bib
	latexmk -pdf -f -pdflatex="pdflatex -interaction=nonstopmode" -use-make main.tex

main.bib:
	touch -m references.bib

clean:
	latexmk -CA
	rm main.bbl
