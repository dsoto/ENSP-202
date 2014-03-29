prefix = 202-lecture
EXT = md
SRC = $(wildcard *.$(EXT))
PDFS = $(SRC:.md=.pdf)
all: $(PDFS)

%.pdf: %.md
	pandoc -t beamer $< -o $@

slidebuild : $(prefix).md
	pandoc -t beamer -i $(prefix).md -o $(prefix).pdf

lecture:
	make slidebuild
	open -a /Applications/Adobe\ Reader.app/ $(prefix).pdf

past:
	cat lecture-*.md > $(prefix)-past.md

