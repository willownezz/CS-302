#/--------------------------------------------------------------------------------------/#
#/ File Name : Makefile                                                                 /#
#/ Version   : 5                                                                        /#
#/ Author    : Luiz Diego Garcia                                                        /#
#/                                                                                      /#
#/ Compiler  : Ubuntu 16.04 - GCC 5.4                                                   /#
#/                                                                                      /#
#/                                                                                      /#
#/                                                                                      /#
#/                                                                                      /#
#/--------------------------------------------------------------------------------------/#

IDIR =../include
CC=gcc
CFLAGS=-I$(IDIR)

ODIR=obj
LDIR =../lib

LIBS=-lm

_DEPS = hellomake.h
DEPS = $(patsubst %,$(IDIR)/%,$(_DEPS))

_OBJ = hellomake.o hellofunc.o
OBJ = $(patsubst %,$(ODIR)/%,$(_OBJ))

$(ODIR)/%.o: %.c $(DEPS)
# $(OBJ): $(ODIR)/%.o: scr/%	.c $(DEPS)
	$(CC) -c -o $@ $< $(CFLAGS)

hellomake: $(OBJ)
	$(CC) -o $@ $^ $(CFLAGS) $(LIBS)

.PHONY: clean

clean:
	rm -f $(ODIR)/*.o *~ core $(INCDIR)/*~
