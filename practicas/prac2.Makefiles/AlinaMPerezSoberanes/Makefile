PROYECTO=muestreo
DESTDIR=/usr/local/bin
CFLAGS=-Wall
LDFLAGS=-lm
CC=gcc
files=muestreo.o procesamiento.o archivos.o

all: $(PROYECTO)
%.o: %.c
	$(CC) -c $< $(CFLAGS)
$(PROYECTO): $(files)
	$(CC) $^ -o $@ $(LDFLAGS)
.PHONY: clean
install: all
	if [ ! -d $(DESTDIR) ]; then \
		sudo mkdir $(DESTDIR); \
	fi; \
	sudo cp $(PROYECTO) $(DESTDIR)
clean: 
	rm -f *.o $(PROYECTO)
uninstall: 
	sudo rm $(DESTDIR)/$(PROYECTO)
