# this makefile is no longer necessary since the various phase is now implemented in python
# just kept here for the record


html:
	mkdir -p $(BUILDDIR)
	$(SPHINXBUILD) -q -b html $(ALLSPHINXOPTS) $(BUILDDIR) -w $(SHINXERRORSOUT) 2>/dev/null
	python $(SCRIBESINFRA)/sphinxproblems problemsToRST $(GROUPDIR) $(BUILDDIR)
	$(SPHINXBUILD) -Q -t sphinx-problems-rerun -b html $(ALLSPHINXOPTS) $(BUILDDIR)
	python $(SCRIBESINFRA)/sphinxproblems patchHTMLFiles $(GROUPDIR) $(BUILDDIR)
	echo "\nOpen $(BUILDDIR)/index.html in a browser to see the documentation"





