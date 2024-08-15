BASE=../base

include ../kernel/config.mk

LIBS=$(patsubst %.c,%,$(wildcard *.c))
LIBS_X=$(foreach lib,$(LIBS),$(BASE)/lib/libsirius_$(lib).so)

CFLAGS= -Os -std=gnu11 -I../base/usr/include -fplan9-extensions -Wall -Wextra -Wno-unused-parameter -L../base/lib -lc
CFILES_UNIVERSAL := $(shell find etc img net tk -type f -name '*.c')
override OBJ := $(addprefix obj-$(KARCH)/,$(CFILES:.c=.c.o))
override HEADER_DEPS := $(addprefix obj-$(KARCH)/,$(CFILES:.c=.c.d))


.PHONY: libs
libs: $(LIBS_X)
	@echo -e 'CC' $@
	@$(KCC) $(CFLAGS) $(CFILES_UNIVERSAL)

SOURCE_FILES = $(wildcard */*.c)
SOURCE_FILES += $(wildcard $(BASE)/usr/include/*.h $(BASE)/usr/include/*/*.h $(BASE)/usr/include/*/*/*.h)
