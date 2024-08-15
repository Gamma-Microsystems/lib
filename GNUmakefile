BASE=../base

include ../kernel/config.mk

LIBS=$(patsubst %.c,%,$(wildcard *.c))
LIBS_X=$(foreach lib,$(LIBS),$(BASE)/lib/libsirius_$(lib).so)

CFLAGS= -Os -std=gnu11 -I. -fplan9-extensions -Wall -Wextra -Wno-unused-parameter

.PHONY: libs
libs: $(LIBS_X)

SOURCE_FILES = $(wildcard */*.c)
SOURCE_FILES += $(wildcard $(BASE)/usr/include/*.h $(BASE)/usr/include/*/*.h $(BASE)/usr/include/*/*/*.h)
