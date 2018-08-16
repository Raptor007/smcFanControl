CC = gcc
CFLAGS = -mmacosx-version-min=10.4 -Wall -g -DCMD_TOOL_BUILD
LDFLAGS = -framework IOKit

all: smc 

smc: smc.o
	$(CC) $(CFLAGS) $(LDFLAGS) -o smc smc.o

smc.o: smc.h smc.c
	$(CC) $(CFLAGS) -c smc.c

clean:
	-rm -f smc smc.o

install:
	cp smc /usr/local/bin/

.PHONY: all clean
