all: example-05.06

example-05.06: lex.yy.o y.tab.o
	gcc -o example-05.06 lex.yy.o y.tab.o -ll

lex.yy.o: lex.yy.c
	gcc -c lex.yy.c

y.tab.o: y.tab.c
	gcc -c y.tab.c

lex.yy.c: ch1-05.l
	lex ch1-05.l

y.tab.c: ch1-06.y
	yacc -d ch1-06.y

clean:
	rm -f *.c *.o example-05.06
