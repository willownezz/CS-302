#////////////////////////////////////////////////////////////////////////////////////////
#///
#/// FILE NAME:        Makefile
#/// DESCRIPTION:      Example functional code
#/// COMPILER:         GNU G++ 5.4 on Linux Ubuntu 16.04
#/// IDE/MEDIUM:       VSCode
#///
#/// MODIFICATION HISTORY:
#/// Author                Date            Ver.     Details
#/// -----------------     ----------      -----    -------------------------------------
#/// Luiz Diego Garcia     2019-09-02      1.0.0    Created file
#///
#////////////////////////////////////////////////////////////////////////////////////////

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
