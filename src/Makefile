CC = gcc
# nombre del ejecutable
TARGET = tp0
TARGET2 = test_utils
NAME = Makefile
# para obtener lista de archivos .c en el directorio.
FUENTES ?= $(wildcard *.c)
HEADERS = $(wildcard *.h)
#OBJS = $(patsubst %.c,%.o,$(FUENTES))
OBJS = tp0.c utils.c utils.h
OBJS2 = test_utils.c utils.c utils.h
FILES = entrada.txt textoCodificado.txt pruebaBinario.bin textoBinarioCodificado.bin tp0_informe.pdf
CC_FLAGS = -g -std=c99 -Wall -Werror -pedantic

all: $(TARGET) $(TARGET2)

%.o: %.c
	echo "Target $@ -> Compilando $<"
	$(CC) -c $(CC_FLAGS) $<


$(TARGET): $(OBJS)
	$(CC) $(CC_FLAGS) -o $(TARGET) $(OBJS) $(LDFLAGS)

$(TARGET2): $(OBJS2)
	$(CC) $(CC_FLAGS) -o $(TARGET2) $(OBJS2) $(LDFLAGS)

clean:
	$(RM) *.o $(TARGET) $(TARGET2) $(TARGET).zip

entrega:
	zip $(TARGET).zip $(FUENTES) $(HEADERS) $(NAME) $(FILES)

.PHONY: all clean
