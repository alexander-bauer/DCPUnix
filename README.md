OK, I'm new to git, so let me know if there's a better way to do this.

WHAT WE HAVE TO WORK WITH:

In the original_v6 directory you will find the original, unmodified Version 6 Unix source code.

The original source code was obtained from http://minnie.tuhs.org/cgi-bin/utree.pl

As far as I can tell, to compile Version 6 Unix on the PDP-11, one would navigate to "/usr/source"
and execute "sh run"

WHAT WE NEED TO DO:

1. The PDP-11 assembly needs to be translated to DCPU16 assembly.
2. The pre-ANSI C needs to be translated to modern C (specifically, C that we can compile using available DCPU tools).
3. Low-level system code needs to be modified to work with the DCPU