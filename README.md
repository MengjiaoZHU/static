# Static Site Builder

In this assignment, you are going to be creating a (simple) static site builder for blogs.

## Example

Given the [`examples/simple/`](examples/simple/) as the input, which looks like this:

```
examples/
— simple/
  — page1.txt
  — page2.txt
```

running the following:

```bash
./generate.sh examples/simple/ output/
```

should create:

```
output/
— page1.html
— page2.html
```

If [`examples/simple/post1.txt`](`examples/simple/post1.txt`) contains

```
Post 1 Title

This is the body of Post 1.
```

then `output/post1.html` should look like

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Post 1 Title</title>
  </head>
  <body>
    This is the body of Post 1.
  </body>
</html>
```

## Requirements

* The script takes two arguments:
    1. The input directory
    1. The output directory
* Given an input directory of plain text files, your script should convert each one to an HTML page the output directory.
* The first line of each text file is the title, and the rest is the body.
* The generated pages should use the provided [template HTML file](template.html), replacing the `{{title}}` and `{{body}}`.
* If the output directory doesn't exist, create it and any missing parent directories (a.k.a. "recursively").

Fill in the [`generate.sh`](generate.sh) shell script with your code. You should not need to modify any other files.

## Things you might need

* Loop(s)
* `sed`
* `head`
* `tail`
* Shell variables
* Shell script arguments

## Run tests locally

```bash
# install test runner
pip install -U pytest
# run tests
pytest -sv
```
