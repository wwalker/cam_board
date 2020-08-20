# useful_scripts

## mkFromCode

Generate markdown from source code files. 
In conjunction with *pandoc* this is 
a useful tool to create lecture notes
and presentations.

Examples of annotation are available in:

```
example.py
```

To generate markdown from this file run:

```bash
$ ./mkFromCode -i example.py -o example.md
```

For more information run:

```bash
$ ./mkFromCode --help
```

### STATUS

- very poorly tested

### TODO

- clean up code, esp loops and nested if elseif ...
- pack reusable code to functions

## keyDir

Simple file manager. Directories can be tagged
and have keywords associated with them via a 
hidden .hdKeys file. 
Methods for filtering these directories using
logical | and & operators will be added (TODO).
Directory choice will be via fzf (TODO).

Additional functions can be added to a .bashrc
file from the output of:

```bash
$ ./keyDir --bashrc
```
For more information run:

```bash
$ ./keyDir --help
```

### STATUS

- very poorly tested

### TODO

- clean up code
- pack reusable code to functions
- implement directory choice via fzf (letting go of this one)

## xoj_present

Turn files created using xournal or xournalpp into beamer style presentations.

Example of turning notes into a presentation:

```bash
$ ./xoj_present notes.xopp presentation_from_notes.xopp simpleparse
```

Example of turning notes into a fancy presentation with sections and subsections (more documentation is needed):

```bash
$ ./xoj_present notes.xopp fancy_presentation_from_notes.xopp parse
```

More information (needs more documentation):

```bash
$ ./xoj_present --help
```

### STATUS

- using an xml parser in python scrambles the order of key value pairs in <... key = value ...>
  this causes xounnal (not sure if xournalpp) to crash, the xml files are reshuffled line by line.

### TODO

- add more documentation to --help 
- clean up code


