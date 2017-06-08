all: dropwatch
CFLAGS+=-c -g -D_GNU_SOURCE -Wall -Werror
LDFLAGS=-lbfd -lreadline -lnl-3 -lnl-genl-3
OBJFILES := main.o lookup.o\
	 lookup_bfd.o lookup_kas.o

dropwatch: $(OBJFILES) 
	gcc -I/usr/include/libnl3/ -g -o dropwatch $(OBJFILES) $(LDFLAGS) 

%.o: %.c
	gcc -I/usr/include/libnl3/  $(CFLAGS) $<
clean:
	rm -f dropwatch *.o

