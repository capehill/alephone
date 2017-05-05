# Makefile for AmigaOS 4

SRC= error.c http.c libnat.c os_common.c os_unix.c ssdp.c upnp.c \
utility.c

OBJ=$(SRC:.c=.o)

liblibnat.a: $(OBJ)
	ar -ru $@ $(OBJ)
	ranlib $@

%.o:%.c
	gcc $(CFLAGS) -c $< -o $@

clean:
	delete #?.o
	delete #?.a