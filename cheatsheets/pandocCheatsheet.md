# Getting started with pandoc
### Installation
```
brew install pandoc   # install pandoc using homebrew
pandoc --version      # verify pandoc is installed
```

### Conversion
```
pandoc test1.md -s -o test1.html   # convert to html
pandoc test1.md -s -o test1.tex    # convert to tex
pandoc test1.md -s -o test1.docx   # convert to docx
pandoc test1.md -s -o test1.pdf    # convert to pdf
```

### Help
```
pandoc --help
man pandoc
```

## Reference
[pandoc.org](http://pandoc.org/installing.html)
[GitHub Flavored Markdown Spec](https://github.github.com/gfm)
