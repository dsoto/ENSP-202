EXT = tex
SRC = $(filter-out solution.tex, $(wildcard *.$(EXT)))
PDFS=$(SRC:.tex=.pdf)
all: $(PDFS)

# generate both the assignment and the solution
# $@ name of target
# $* stem of target
# $< name of first prerequisite

%.pdf: %.$(EXT)
	# create solution
	echo "\solutiontrue" > solution.tex
	pdflatex $<
	mv $@ $*-solution.pdf
	# create assignment
	echo "\solutionfalse" > solution.tex
	pdflatex $<

tidy:
	rm *.log *.aux
	rm solution.tex
