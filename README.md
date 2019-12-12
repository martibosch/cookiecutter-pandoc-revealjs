# cookiecutter-pandoc-revealjs

My personal [cookiecutter] template for [reveal.js](http://revealjs.com/) slides rendered via [pandoc] markdown.

## Instructions to run locally

1. Use cookiecutter to create the template folder structure
   
    ```
    $ cookiecutter gh:martibosch/cookiecutter-pandoc-revealjs
    ```
    
2. Edit the file `slides.md` in the generated folder

3. Use the provided Makefile to generate the slides

    ```
    $ make slides
    ```
    
4. Open the generated `index.html` in your browser

## Instructions to deploy to GitHub

1. Do the steps 1-3 from the list above

2. Create a git repository from the root of the generated folder

    ```
    $ git init
    ```

3. Commit the files (you need to include `index.html` and all images in the `media` folder)

    ```
    $ git add .
    $ git commit -m "created slides"
    ```
    
4. Create a GitHub repository and push your local repository there

5. Go to the "Settings" tab of the GitHub repository, scroll down to the "GitHub Pages" section and choose "master branch" in the selection box

6. Wait until the website is deployed (e.g., refresh the "Settings" page), and then the green flash message will show you where the slides can be viewed online (e.g., https://{{username}}.github.io/{{repository}})


## Requirements

This repository requires [cookiecutter] and [pandoc], which can be easily installed with conda as in:

    $ conda install -c conda-forge pandoc cookiecutter

## TODO

* Local server with auto-refresh to preview the slides (e.g., with [watchdog](https://github.com/gorakhargosh/watchdog))

## Acknowledgments

* Original idea from Nick Groenen ([zoni](https://github.com/zoni))

[cookiecutter]: https://cookiecutter.readthedocs.io/
[pandoc]: https://www.pandoc.org/
