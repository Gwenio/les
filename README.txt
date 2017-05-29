= LES

== DESCRIPTION:

LES (Lisp Erlang Smalltalk) is a language based on the Kernel Lisp dialect
that draws much inspiration from Elixir and Pharo Smalltalk.

The goal is a language with a self contained development environment similar
to Smalltalk that facilitates designing Domain Specific Languages (DSLs) and
getting them to run in the environment and take advantage of the development
tools in it.

Furthermore, the goal is to also provide tools to make it simple to generate
code from sources in DSLs in a language that can be used in projects it is for.

DSLs allow for readable and concise code for the problem domain they work on.
Furthermore, knowing what code is being used for means high level optimization
can be preformed if the tooling exists.

By making it easier to create DSLs LES aims at making programs with common
design patterns easier to write quickly and robustly.

A great example is compilers where the various passes of lexical analysis,
parsing, semantic analysis, generating intermediate code, optimizing the
intermediate form, and generating the output each have elements that
tend to be common across different compilers regardless of the source
and output language.

== FEATURES (Planned):

Data is code, and code maps directly to data primitives. And the structure of
its basic data structures model ASTs, allowing DSL to be executed directly
after parsing them.

First class environments and operatives. Inherited from Kernel, operatives
are a combination of closures and macros, removing the need for quotation
and special forms that keep many Lisp dialects from having code and data
truly be the same.

First class continuation and coroutines allow flexible control flow to
model any operation ordering a DSL might need.

Sane model for updating program state in the presence of garbage collection.
Garbage collected languages that do not provide tools to manage mutation
present more problems than multi-threading in languages that have the
programmer deal with memory management as controlling mutation is trivial
if you have already tracked down the life span of every piece of data.

Proper tail recursion.

Good modelling of distributed code while having it all in one program,
allowing for easier debugging.

Extensive development tools that can be hooked up to also work with code
written in DSLs implemented on top of LES.

Persistent state similar to Smalltalk.

The language created for the reference interpreter (PLES) serves an easy output
target for making stand alone programs from DSL code.

== BUILDING:

	Currently the boot strap programs are in need of updating.
Building would require writing such a program based on the documentation in
the design folder.

== REQUIREMENTS:

Not applicable at this time.

== PROJECT LAYOUT:

- build			: Contains build specification files
- design		: Contains documents about the design of LES and associated languages.
- macro			: Contains macros to pre-process source files with.
- src			: Contains the source files that have not been expanded to PLES.
					Code is place in sub folders based on the name of its build file.
- TODO.txt		: Lists work planned.
- LICENSE		: The license for the project's code.
- README.txt	: This file.

== DEVELOPERS:

Adam Armstrong

== LICENSE:

The project's code is under the ISC license, see the LICENSE file for details.

It is also included in files along side the source code.
