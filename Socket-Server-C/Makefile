default: build

build:
	gcc -o server src/main.c

run: build
	./server

tests:
	checkmk test/test.ts > test/test.c
	gcc -o run_tests src/backend.c src/backend.h test/test.c -lcheck
	./run_tests

clean:
	rm server run_tests
