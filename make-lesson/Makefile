include config.mk

TEXT_FILES=$(wildcard books/books/*.txt)
DATA_FILES=$(patsubst books/books/%.txt, %.dat,$(TEXT_FILES))
#Generate summmery table

results.txt : $(ZPF_SRC) $(DATA_FILES)
	$(ZIPF_EXC) $(DATA_FILES) > $@
	
#Count words
.PHONY : dats
dats : $(DATA_FILES)

%.dat : books/books/%.txt $(COUNT_SRC)
	$(COUNT_EXC) $< $@

.PHONY : variables
variables:
        @echo TEXT FILES: $(TEXT_FILES)
        @echo DATA_FILES: $(DATA_FILES)

.PHONY : clean
clean : 
	rm -f $(DATA_FILES)
	rm -f results.txt

.PHONY : variables
variables:
	@echo TEXT FILES: $(TEXT_FILES)
	@echo DATA_FILES: $(DATA_FILES)
