# Project: hw1
# Author: Erik Anderson
# Date: 09/03/2022

MAIN:=main
default:=generated/$(MAIN).pdf

# Builds twice for references and toc 
$(default): $(MAIN).tex student.sty
	pdflatex $(MAIN).tex
	pdflatex $(MAIN).tex > /dev/null 2>&1 
	mkdir -p generated 
	mv $(MAIN).log $(MAIN).aux $(MAIN).pdf generated/

# Open up the generated pdf with evince after build
.PHONY: view 
view: $(default) 
	evince generated/$(MAIN).pdf

.PHONY: clean 
clean:
	rm -rf generated/ 

