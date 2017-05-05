# Makefile for AmigaOS 4

SRC= xmlparse.c xmlrole.c xmltok.c xmltok_impl.c xmltok_ns.c


OBJ=$(SRC:.c=.o)

libexpat.a: $(OBJ)
	ar -ru $@ $(OBJ)
	ranlib $@

%.o:%.c
	gcc $(CFLAGS) -c $< -o $@

clean:
	delete #?.o
	delete #?.a
