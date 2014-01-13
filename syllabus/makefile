prefix = 202-syllabus

all : $(prefix).html $(prefix).pdf

$(prefix).html : $(prefix).md
	pandoc -o $(prefix).html -c soto.css $(prefix).md

$(prefix).pdf : $(prefix).html
	wkpdf -p letter -m 36 -o $(prefix).pdf -s $(prefix).html
