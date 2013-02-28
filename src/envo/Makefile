# This Makefile is for use by the ENVO Release Manager (currently cjm)
# Also used by Jenkins: http://build.berkeleybop.org/job/build-envo
# 
# requirements: Oort (http://code.google.com/p/owltools/wiki/OortIntro)
#
# To make a release, type 'make release' in this directory

release: envo-basic.obo

# all release files are derived from the editors version.
# we use the default Oort setup (hermit as reasoner)
envo-simple.obo: envo-edit.obo
	ontology-release-runner --run-obo-basic-dag-check --error-report envo-errors.txt $< --allow-overwrite --asserted --simple
.PRECIOUS: envo.obo

envo-basic.obo: envo-simple.obo
	cp envo-simple.obo $@
