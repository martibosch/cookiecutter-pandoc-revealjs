PANDOC_FLAGS =\
	-t revealjs --slide-level 1
REVEALJS_VARIABLES =\
	-V fragments=false -V transition=none -V controls=false -V slideNumber=false

html: $(patsubst %.md,%.html,$(wildcard *.md))

%.html: %.md Makefile
	pandoc $(PANDOC_FLAGS) $(REVEALJS_VARIABLES) -s $< -o $@
