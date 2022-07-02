default: build

build:
	gcc -o client src/main.c

run: build
	./client

tests:
	checkmk test/test.ts > test/test.c
	gcc -o run_tests src/backend.c src/backend.h test/test.c -lcheck
	./run_tests

clean:
	rm client run_tests
