# Labels

Generates a PDF document from a CSV file to print sticker labels.

<a href="sample.pdf"><img src="image.png" width="600px"></a>

It is, surprisingly, a very tricky/annoying thing to do. There is software out there for doing this, but you have to pay yearly plans just to generate a few pages. Sometimes they do not have the type of stickers you need, or the correct number of rows or columns. Furthermore, after all of that, some printers do not handle margins correctly or lie about it.

This simple script takes a CSV file and uses [Prawn](http://prawnpdf.org). This allows you to set all those parameters manually to get them right. With a little bit of trial and error the correct PDF document is ready for printing.

[🖨 Take a look to the PDF sample](sample.pdf)

### How to use

1. Install gems with `bundle install`

2. Drop CSV data inside `data.csv`. Format: `Name, Company, Address line 1, Address line 2, Country`

3. Tweak params inside the `bin/generate` file to match your paper/printer

4. Run `bin/generate` to generate the PDF

### Tips for printing

- Page default is `A4`, but always choose `A4 borderless` when printing

- Always scale to `100%` so each sticker gets correctly aligned to its spot

- Measure page size, margins and gutters and tweak parameters inside `bin/generate`

- If you run into layout problems there is a `debug` flag
