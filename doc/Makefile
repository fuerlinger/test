all : NArray

NArray : NArray.html NArray.pdf #NArray.txt

%.html : %.md
	pandoc -s -o $@ $+ -c github.css --default-image-extension=svg

%.pdf : %.md
	pandoc -V fontsize=12pt --number-sections --listings -H listings-setup.tex -o $@ $+ --default-image-extension=pdf

%.txt : %.md
	pandoc -o $@ -t asciidoc $+

clean :
	rm -f NArray*.html NArray*.pdf NArray*.txt
	rm -f *~

