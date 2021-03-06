# Parser for .bbl files

This repo provides a python script to extract and print as plain text the
bibliography from a `.bbl` generated with BibTeX when compiling the bibliography for
a LaTeX document. This is very useful when journals ask for the bibliography in
`txt` format. The script also converts the text in LaTeX format to utf-8 so the
accents and special characters are well represented. Note that the bibliography 
items in the `.bbl` files appear in the same order as in the final pdf.

Currently, the script has only been tested with few `.bbl` files so be sure you
always check its output. Suggestions for improving the tool are welcome so do
not hesitate in sending a pull request or open an issue.

# Usage

If you run the script adding the path to the `.bbl` file as argument:

```
python3 parse_bbl.py path/to/the/file.bbl
```

It will print the bibliography in the terminal with one item per line numerated as:

```
[1] First bibliography item.
[2] second bibliography item.
.
.
.
```

For more specific usages you can use the `BibItem` and the `BblFile`
classes defined in the script (see their documentation for more information).

## Requirements

Python 3.6 or later is required. On the other hand, the conversion from LaTeX to
utf-8 is handled by the `pylatexenc` packages so make sure you have it
installed:

```
python3 -m pip install pylatexenc
```

