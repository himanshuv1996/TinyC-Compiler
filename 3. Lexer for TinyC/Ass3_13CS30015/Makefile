a.out : lex.yy.o ass3_13CS30015.o y.tab.o
	gcc lex.yy.o ass3_13CS30015.o y.tab.o -lfl
	echo "Enter "make run" to run the test file."
y.tab.o : y.tab.c y.tab.h
	gcc -c y.tab.c
lex.yy.o: lex.yy.c
	gcc -c lex.yy.c
lex.yy.c: Ass3_13CS30015.l y.tab.h
	flex Ass3_13CS30015.l
ass3_13CS30015.o : ass3_13CS30015.c y.tab.h
	gcc -c ass3_13CS30015.c
y.tab.h: Ass3_13CS30015.y
	yacc -dtv Ass3_13CS30015.y
y.tab.c: Ass3_13CS30015.y
	yacc -dtv Ass3_13CS30015.y
clean:
	rm a.out lex.yy.o ass3_13CS30015.o lex.yy.c y.tab.c y.tab.h y.tab.o y.output
run:
	./a.out < Ass3_13CS30015_test.c
