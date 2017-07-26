name = cv

tex = $(name).tex
pdf = $(name).pdf

$(pdf): $(tex)
	latexmk -pdf $(tex)

html: $(tex)
	mkdir -p $@
	latex2html -dir $@ -split +0 $(tex)

.PHONY: edit-compile-view-loop
edit-compile-view-loop:
	latexmk -pdf -pvc $(tex)

.PHONY: clean
clean:
	latexmk -c
	rm -rf html

.PHONY: nuke
nuke:
	latexmk -C
	rm -rf html
