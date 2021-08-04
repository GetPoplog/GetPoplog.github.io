---
sort: 3
---
# The Pop-family of Programming Languages

Although not widely known outside the UK, the Pop-family of programming languages is surprisingly old and has many branches. Originated by Robin Popplestone at the University of Edinburgh around 1966-8 as COWSEL / POP-1, it gained traction with the publication of the [POP-2 Papers](http://www.cs.otago.ac.nz/staffpriv/ok/pop2.d/POP-2_Papers_1968.pdf) by Burstall, Collins and Popplestone, which is an elegant and persuasive account of the language and its intellectual underpinnings.

POP-2 is both recognisable and even readable to today's Pop-11 programmers. It was a workhorse for AI research in the UK in the 1970s and spawned a variety of variants. Although it remained something of an 'underground hit' for researchers, it represented a fascinating alternative to the near-hegemony of Lisp. As [Richard O'Keefe writes](http://www.cs.otago.ac.nz/staffpriv/ok/pop2.htm) "The influence of Pop-2 has been more than you might imagine. Traces of Pop-2 syntax can still be found in Standard ML, in Prolog, and in Erlang."

## Family Tree

The following graph shows the rapid development and mutation of Pop-variants. All of these shared a foundation of an open value stack that was separately from the call-stack, human-friendly, extensible, non-homoiconic syntax, first class functions, quasi-quoted lists and dynamic lists for I/O.

<div align="center"><img src="FamilyTree.png" alt="A tree showing the lineage of Pop-11 starting from Pop-1"/></div>

## Incomplete

Unfortunately the interesting history of variants is not well known. However there were significant efforts, such as PopTalk. This was a commercial language used as part of MUSE, an expert system developed by Cambridge Consultants Ltd. (And if anyone has knowledge of PopTalk and would like to get in contact, it would be great to learn more about it!)