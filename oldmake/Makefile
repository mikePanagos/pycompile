run: calc
	./calc
calc: lex.yy.c y.tab.c
	g++ -g lex.yy.c pythoninterpreter.tab.c -o calc

lex.yy.c: y.tab.c pythoninterpreter.l
	flex pythoninterpreter.l

y.tab.c: pythoninterpreter.y
	bison -d pythoninterpreter.y

clean: 
	rm -rf lex.yy.c pythoninterpreter.tab.c pythoninterpreter.tab.h calc calc.dSYM
