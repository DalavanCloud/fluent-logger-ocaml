SRCS=fluent_logger_test.ml stream_sender_test.ml
REQUIRES=unix,msgpack,ounit

.PHONY: all run clean

all: run

fluent_logger_test: $(SRCS)
	$(OCAMLC) -thread -I ../lib -o $@ -package "$(REQUIRES)" ../lib/fluent_logger.cma -linkpkg $(SRCS)

run: fluent_logger_test
	./fluent_logger_test

clean:
	rm -rf fluent_logger_test *.cmi *.cmo
