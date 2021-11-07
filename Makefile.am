CC = gcc
CFLAGS = -Wall -O6 -fcommon

UNAME := $(shell uname)
ifeq ($(UNAME), Linux)
SCEDOORMAT_EXE	= bin/SCEDoormat_NoME
else
SCEDOORMAT_EXE	= bin/SCEDoormat_NoME.exe
endif

SCEDOORMAT_SRC	= public/scedoormat.c public/khn_fs.c public/khn_maths.c
SCEDOORMAT_OBJ	= $(SRC:.c=.o)

.PHONY: all
all: $(SCEDOORMAT_EXE)

.PHONY: clean
clean:
	rm -f *.o *.s $(SCEDOORMAT_EXE)

$(SCEDOORMAT_EXE): $(SCEDOORMAT_SRC)
	$(CC) -o $@ $^ $(CFLAGS)

%.o: %.c
	$(CC) -o  $@ -c $< $(CFLAGS)
