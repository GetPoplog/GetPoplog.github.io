# Welcome to GetPoplog

Poplog is an old-school, open source AI development system for four programming languages: Pop-11, Prolog, Common Lisp and Standard ML. 

<div align="center">
<a href="Download.html"><img src="download.png" alt="Download Poplog"/></a>
<p><em>Binary distributions built for Linux systems</em></p>
</div>

## Why Poplog?

Poplog is an open source, incrementally compiled software development environment for the programming languages POP-11, Common Lisp, Prolog, and Standard ML, originally created in 1981 at the University of Sussex. It was initially used for teaching and research in Artificial Intelligence and later marketed as a commercial package for software R&D. Despite being remarkably innovative, anticipating many major language development themes by several decades, organised development on Poplog ground to a halt in the late 1990s. Fortunately it was made open source by the University of Sussex and has since been maintained by enthusiasts.

Why the renewed interest in this venerable system? I reflected on this topic at ECOOP in 2019, where I gave a retrospective on Poplog and highlighted some of its features that have contemporary interest, such as the four supported REPL interpreters (plus foreign function interface), the unique and efficient language extensibility in non-homoiconic, human-friendly language, concatenative semantics, abstraction over assignment, generalised coroutines that include generators and fibres as special cases, dynamic localisation as an alternative to dependency injection, unrestricted closures in a fully imperative language and more. In fact it was remarkably ahead of its time and it remains a source of inspiration as well as being a very practical system. You can read the [whole presentation here](https://docs.google.com/presentation/d/e/2PACX-1vSWFYh1OCBXk3i_O_8J44BsWfm03ftpdLMMzht7F6jDRHgUW5-7wgZQWFuSyooMk394ubTqH7SAPMRq/pub?start=false&loop=false&delayms=60000). 


## Our Aims

We aim to automate of the production and test of reliable, easy-to-use, simple installation methods for Poplog that deliver a well-organised but flexible installation.
- By reliable we mean that it copes with a wide variety of distributions without intervention
- By easy-to-use we mean that it uses well-established packaging mechanisms on our target platforms
- By simple we mean that users can immediately use it after installation without changing login scripts
- By well-organised we mean that its installed commands and environment-variables are few and well-grouped together
- By flexible we mean that advanced users can easily configure the full array of Poplog commands and linkage by environment variables.

This work is only possible thanks to [Aaron Sloman](https://www.turing.ac.uk/people/researchers/aaron-sloman)'s dedication in maintaining
the [FreePoplog](https://www.cs.bham.ac.uk/research/projects/poplog/freepoplog.html) resource over the years.

