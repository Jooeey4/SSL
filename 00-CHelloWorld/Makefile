# Macros

CC = gcc
CFLAGS = -g 
OUT_PATH = out/
SRC = hello.c
OBJ = hello.o

# Explixit Rules

all: $(OBJ)
		mkdir $(OUT_PATH) && $(CC) $(CFLAGS) -o $(OUT_PATH)hello $(OBJ)

clean:
		$(RM) -rf $(OBJ) $(OUT_PATH)

# Implcit Rules

hello.o: hello.c
