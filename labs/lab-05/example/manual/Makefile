all: dynamic_block static_block

clean:
	rm dynamic_block static_block program.o dynamic_lib.so static_lib.a block.o

static_block: program.o static_lib.a
	gcc program.o static_lib.a -o static_block

dynamic_block: program.o dynamic_lib.so
	gcc program.o dynamic_lib.so -o dynamic_block -Wl,-rpath='$$ORIGIN'

dynamic_lib.so: block.o
	gcc -shared -o dynamic_lib.so block.o

static_lib.a: block.o
	ar rcs static_lib.a block.o

block.o: source/block.c headers/block.h
	gcc  -fpic -c source/block.c -o block.o

program.o: program.c
	gcc -c program.c -o program.o