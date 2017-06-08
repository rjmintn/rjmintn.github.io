---
layout: post
title: RJ v2.0
---

# The Beginning

I can remember seeing my first desktop computer system in the school library. It’s black keyboard and steel gray plastic case sat on a table in one of the back study rooms. No mouse. No display color from the monitor. Not because they were missing or broken as it was designed that way. The librarian showed me the basics on turning it on, using some of the programs that came with it, and soon I was on my own. I started learning to write programs for fun. A few ‘for - next’ loops, some ‘if - then - else’ decisions. The basics. Literally,  BASIC. It was 1983 and that computer was a [TRS-80](https://en.wikipedia.org/wiki/TRS-80) with a single 5.25” 180Kb floppy drive to save to, a dot-matrix printer, and a display resolution of 64 columns by 16 rows of ASCII characters. It was AWESOME.

At home I remember a [Commodore 64](https://en.wikipedia.org/wiki/Commodore_64) sitting on a desk in the den. I would write programs there as well. Not as much fun until the tape cassette storage device was purchase and I could actually SAVE programs that were created. That was followed by an [Apple IIe](https://en.wikipedia.org/wiki/Apple_IIe) clone with a built in floppy drive. I was in heaven! I would spend hours typing in lines of code out of books that listed complete programs, fixing typos, making little changes and seeing the effect.

A few years later, I was taking courses at the local community college. Assembler, COBOL, Fortran… I worked nightshift at a small software product packaging company where we would use high speed diskette duplicators that could copy 1.2Mb 5.25” and 1.44Mb 3.5” diskettes in 2 minutes, label the disks, put the media and documentation into the packaging, shrink wrap send them to the distributor. One evening, of the daytime managers came to me with a floppy disk and a handwritten note:

> Convert [EBCDIC](https://en.wikipedia.org/wiki/EBCDIC) → [ASCII](https://en.wikipedia.org/wiki/Extended_ASCII)  
> 240 - 249 = 48 - 57  
> 193 - 198 = 65 - 70  
> 64 = 32  

He explained the situation and requirements. A customer was moving from an IBM mainframe to an Intel server/client network and needed their data files converted so the new system could read it. The data was hexadecimal numerals arranged in columns of various widths and those columns and widths varied between each file. Within the file, the data structure would be identical from beginning to end and each line of data was marked with a carriage return. Which made it easy because EBCDIC and ASCII used the same code for a CR. The files were too large to be fully read into memory, converted, and written.

My first paid programing job! This was 1990 and the current MS-DOS version was 4.01 which came with GW-BASIC. The solution was fairly straightforward. Essentially read in a line of data into a string, parse through the string one letter at a time, change the letter based on its value, add the converted line to a new file, and repeat until done. I had a minor issue to overcome with the final output. I did not have the actual character maps for [EBCDIC or ASCII](http://www.simotime.com/asc2ebc1.htm) and when displaying the finished data the columns were not vertically aligned. An extra non printable character was being added and it would skew the columns. My solution was to cut the last character from the line of data as it was written to disk. It turns out that EBCDIC uses both a CR (carriage return) and LF (line feed) and MS-DOS treats a CR as CRLF.

Up next… Life happens...
