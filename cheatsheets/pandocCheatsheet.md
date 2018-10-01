# Pandoc
If you need to convert files from one markup format into another, pandoc is your swiss-army knife.


### Installation
Refer to [https://pandoc.org/installing.htm](https://pandoc.org/installing.htm) for installation procedures on different operating systems.

### Conversion
Convert markdown file to commonly used file format.
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
