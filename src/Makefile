CC = gcc
CFLAGS = -Wall -g
INCLUDES = -I../../blackc/black/include -I../../blackc/blacklua/include $(shell sdl-config --cflags)
LDFLAGS = -L../ $(shell sdl-config --libs)
LIBS = -lblack -lblacklua -llua -lSDL_ttf -lSDL_mixer -lSDL_image

SRCS = \
	main.c

OBJS = $(SRCS:.c=.o)

MAIN = fallen

.SUFFIXES: .c .o .i

.c.o:
	$(CC) $(CFLAGS) $(INCLUDES) -c $< -o $@

.PHONY: depend clean

$(MAIN): $(OBJS)
	$(CC) $(CFLAGS) $(INCLUDES) -o $(MAIN) $(OBJS) $(LDFLAGS) $(LIBS)

clean:
	rm -f *.o *~ $(MAIN)

depend: $(SRCS)
	$(CC) -M $(CFLAGS) $(INCLUDES) $^ > $@

include depend
