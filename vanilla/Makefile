OPENRESTY_PREFIX=/usr/local/openresty

PREFIX ?=          /usr/local/vanilla
VANILLA_LIB_DIR ?= $(PREFIX)/
INSTALL ?= install

.PHONY: all test install

all: ;

install: all
	$(INSTALL) -d $(DESTDIR)/$(VANILLA_LIB_DIR)/resty/
	$(INSTALL) ./bin $(DESTDIR)/$(VANILLA_LIB_DIR)/bin
	$(INSTALL) ./v $(DESTDIR)/$(VANILLA_LIB_DIR)/vanilla/v
	$(INSTALL) ./sys $(DESTDIR)/$(VANILLA_LIB_DIR)/vanilla/sys
	$(INSTALL) ./vanilla $(VANILLA_BIN_PATH)/vanilla
	$(INSTALL) ./vanilla-console $(VANILLA_BIN_PATH)/vanilla-console

test: all
	PATH=$(OPENRESTY_PREFIX)/nginx/sbin:$$PATH prove -I../test-nginx/lib -r t

