# Copyright (c) 2011 The Chromium OS Authors. All rights reserved.
# Copyright (C) 2009-2014 Broadcom Corporation
# Use of this source code is governed by a BSD-style license that can be
# found in the LICENSE file.

LDLIBS = -lbluetooth

brcm_patchram_plus:	brcm_patchram_plus.c
	$(CC) $(CFLAGS) $(CPPFLAGS)  $(LDFLAGS) -o $@ $< $(LDLIBS)

$(DESTDIR)usr/sbin/brcm_patchram_plus:	brcm_patchram_plus
	echo Installing to location  $(DESTDIR)usr/sbin
	install --mode 555 -D -T $< $@

all:	brcm_patchram_plus

install:	$(DESTDIR)usr/sbin/brcm_patchram_plus

clean:
	rm -f brcm_patchram_plus *.o

.PHONY:		all install clean
