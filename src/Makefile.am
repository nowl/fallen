bin_PROGRAMS = fallen

fallen_SOURCES = \
	main.c

fallen_CFLAGS = -I../../blackc/black/include -I../../blackc/blacklua/include @SDL_CFLAGS@
fallen_LDFLAGS = @SDL_LIBS@ @SDL_MIXER_LIBS@ @SDL_IMAGE_LIBS@ @SDL_TTF_LIBS@ -L../../blackc/black/src -lblack -L../../blackc/blacklua/src -lblacklua -llua
