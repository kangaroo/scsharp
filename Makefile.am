
SUBDIRS= docs SCSharp src tools Tests 

EXTRA_DIST= HACKING

install:
	@echo \"make install\" doesn\'t work yet.  try again later.

dist-hook:
	mkdir -p $(distdir)/sdldotnet-bin
	cp sdldotnet-bin/* $(distdir)/sdldotnet-bin

#dll configs?
RELEASEDIR=$(PACKAGE)-release-$(VERSION)
release: all
	rm -rf $(RELEASEDIR)
	-mkdir $(RELEASEDIR)
	rm -f $(RELEASEDIR).zip
	@cp src/scsharp.exe $(RELEASEDIR)
	@cp src/scsharp.exe.config-example $(RELEASEDIR)/scsharp.exe.config
	@cp SCSharp/*.dll $(RELEASEDIR)
	@cp sdldotnet-bin/*.dll $(RELEASEDIR)
	@cp sdldotnet-bin/*.dll.config $(RELEASEDIR)
	@cp NEWS $(RELEASEDIR)/NEWS
	@cp README $(RELEASEDIR)/README
	@cp AUTHORS $(RELEASEDIR)
	zip -r $(RELEASEDIR).zip $(RELEASEDIR)
	rm -rf $(RELEASEDIR)
