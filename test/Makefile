ML = $(wildcard *.ml)
PROG = $(ML:.ml=)

all:
	@dune build

runtest:
	@dune runtest

rig:
	@dune exec ./rig.exe

test:
	@for p in $(PROG); do echo "\n\n##### Running $$p #####\n"; dune exec ./$$p.exe || exit 1; done

pdf:
	@dune exec ./squierGroup.exe
	pdflatex squierGroupFull.tex
