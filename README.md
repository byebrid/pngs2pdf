# pngs2pdf
A simple command-line tool to convert a series of pngs into a single pdf. Yes, it's very niche but I needed something like this and Mac OS was not very helpful at all (and jesus christ, I do not like bash).

## Recommended setup
---
Make `pngs2pdf` executable and put it in `usr/local/bin`. Or do your own thing.

## Usage
---
- To specify input pngs:
  ```
  $ pngs2pdf example1.png example2.png

  Merging example1.png example2.png...

  Done! See 48b9754a-1d4b-4249-83d8-8aba1992a940.pdf
  ```
  Note that it generates a random pdf name if no `--output` argument is provided.
- To specify output: 
  ```
  $ pngs2pdf -o example_output.pdf example1.png example2.png # or `--output`

  Merging example1.png example2.png...

  Done! See example_output.pdf
  ```
- If you don't specify input pngs:
  ```
  $ pngs2pdf -o example_output.pdf

  Since no pngs have been provided, searching in this directory:
  /Users/RickAstley/Never/Gonna/Give/You/Up.

  Found the following pngs in this directory:
      0: example1.png
      1: example2.png

  Are you sure you would like to merge ALL of the above pngs?
  Y/N: y # User input here

  Merging example1.png example2.png...

  Done! See example.pdf
  ```
