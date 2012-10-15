OK, I'm new to git, so let me know if there's a better way to do this.

#What We have to work with:#
In the original_v6 directory you will find the original, unmodified Version 6 Unix source code.

The original source code was obtained from http://minnie.tuhs.org/cgi-bin/utree.pl

As far as I can tell, to compile Version 6 Unix on the PDP-11, one would navigate to "/usr/source"
and execute "sh run"

#What we need to do:#
1. The PDP-11 assembly needs to be translated to DCPU16 assembly.
2. The pre-ANSI C needs to be translated to modern C (specifically, C that we can compile using available DCPU tools).
3. Low-level system code needs to be modified to work with the DCPU

#Method:#
I propose translating the files in the order they will be compiled according to "/usr/source/run"
(e.g. starting with the C files in "/usr/sys/ken").

From what I understand, the DCPU Toolchain is the most mature set of tools, so we should aim for our C code to be
compliant with their C compiler.