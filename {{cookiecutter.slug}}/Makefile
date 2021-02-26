.PHONY: create_environment slides

create_environment:
	conda env create -f environment.yml

PANDOC_FLAGS = --slide-level {{ cookiecutter.slide_level }} \
	-t revealjs -f markdown{% if cookiecutter.emojis == 'y' %}+emoji{% endif %}
REVEALJS_VARIABLES = -V transition={{ cookiecutter.transition }} \
	-V controls={{ cookiecutter.controls }} \
	-V slideNumber={{ cookiecutter.slide_number }} \
	-V revealjs-url={{ cookiecutter.revealjs_url }}

index.html: slides.md
	pandoc $(PANDOC_FLAGS) $(REVEALJS_VARIABLES) -s $< -o $@

slides: index.html
