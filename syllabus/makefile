all : 202-syllabus.html syllabus.pdf

202-syllabus.html : syllabus.md
	pandoc -o 202-syllabus.html -c soto.css syllabus.md

syllabus.pdf : 202-syllabus.html
	#pandoc -o syllabus.pdf syllabus.md
	# maybe make intermediate html using special pdf.css file?
	# use css on server?
	wkpdf -o syllabus.pdf -m 36 -s 202-syllabus.html
