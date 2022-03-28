# Project: hw2
# Author: Erik Anderson
# Date: 09/03/2022

MAIN:=hw2_soln
default:=generated/$(MAIN).pdf

# Builds twice for references and toc 
$(default): $(MAIN).tex
	pdflatex $(MAIN).tex
	pdflatex $(MAIN).tex > /dev/null 2>&1 
	mkdir -p generated 
	mv $(MAIN).log $(MAIN).out $(MAIN).aux generated/
	cp $(MAIN).pdf generated/

# Open up the generated pdf with evince after build
.PHONY: view 
view: $(default) 
	evince generated/$(MAIN).pdf

.PHONY: clean 
clean:
	rm -rf generated/ 
