all: design.html review.html

%.html: %.txt
	rst2html.py --stylesheet=assets/style.css $< $@.pre
	sed -e '/<\/\?blockquote>/d' -i $@.pre
	mv $@.pre $@

.PHONY: clean

clean:
	@-rm *.html *.html.pre
