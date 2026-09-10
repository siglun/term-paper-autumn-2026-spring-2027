
.SUFFIXES: .pic .ms .pdf .ps .eps 
.DEFAULT: .ms.pdf .ps.pdf .eps.pdf

default: chalmers.pdf 

URI = https://github.com/siglun/term-paper-spring-2026/blob/main/
PAPER = -dpaper=a4 -P-pa4
OTHERS =  ../bib/references.text ../tmac/dropcap.tmac ../tmac/mn.tmac \
	Makefile ../tmac/fitch-macros.pic ../parameters.ms ../margin-notes.ms

.ms.pdf:
	pdfroff -U -R -sGtep   -ms -m pdfmark -m mn \
	-m decorations -m dropcap -M ../tmac   \
	-k  ${PAPER} -Tps  ../parameters.ms   $<  > $*.pdf
	pdftotext $*.pdf ; wc -c $*.txt ; rm  $*.txt


clean:
	rm -f *~ *.eps

chalmers.pdf: chalmers.ms chalmers-01.ms $(OTHERS)


# Remember
#
# inkscape World_line.svg -o  world_line.eps
# 
