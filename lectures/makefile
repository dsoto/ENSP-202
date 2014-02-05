prefix = 202-lecture

lecture.pdf : $(prefix).md
	pandoc -t beamer $(prefix).md -o $(prefix).pdf

past:
	cat lecture-*.md > $(prefix)-past.md
