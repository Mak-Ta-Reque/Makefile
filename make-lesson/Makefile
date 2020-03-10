# Count words.
results.txt : testzipf.py isles.dat abyss.dat last.dat
	python $^ *.dat > $@
	rm -f *.txt
	
	
.PONY : dats
dats : isles.dat abyss.dat last.dat

%.dat : books/%.txt countwords.py
	python countwords.py $< $@

.PONY : clean
clean : 
	rm -f *.dat results.txt
