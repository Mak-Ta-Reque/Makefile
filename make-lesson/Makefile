# Count words.

#Variables
LANGUAGE=python
COUNT_SRC=countwords.py
COUNT_EXC=$(LANGUAGE) $(COUNT_SRC)
ZPF_SRC=testzipf.py
ZIPF_EXC=$(LANGUAGE) $(ZPF_SRC)
DATA=*.dat
results.txt : $(ZPF_SRC) isles.dat abyss.dat last.dat
	$(ZIPF_EXC) *.dat > $@
	
	
.PONY : dats
dats : isles.dat abyss.dat last.dat

%.dat : books/%.txt countwords.py
	$(COUNT_EXC) $< $*.dat

.PONY : clean
clean : 
	rm -f *.dat results.txt
