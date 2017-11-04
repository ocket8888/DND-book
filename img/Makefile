.PHONY: all clean

ASSETS := $(patsubst src/%.svg, dist/%.pdf, $(wildcard src/*.svg))

all: $(ASSETS)

clean:
	$(RM) dist/*.pdf

dist/%.pdf: src/%.svg
	inkscape --export-area-drawing --export-pdf=$(PWD)/$@ --without-gui $(realpath $<)
