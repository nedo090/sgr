
.PHONY: default clean 

default: Dmdns 

Dmdns: ndpi_util.o mdns.o libndpi.a collecmdns.c 
	clang -lpcap $^ -o $@

ndpi_util.o: ndpi_util.c ndpi_util.h
	clang -lpcap $^ -c

mdns.o: mdns.c
	clang $^ -c

clean: 
	rm -f Dmdns
	rm -f *.o

