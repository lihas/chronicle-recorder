Downloaded from https://code.google.com/archive/p/chronicle-recorder/
on 19/08/2016

Getting Started
===============

Run "make all check" to build Chronicle and Valgrind and run a simple
sanity check that everything is working.

Directory Structure
===================

docs/
    Documentation files
valgrind/
    Patched Valgrind including 'chronicle' tool
indexer/
    Helper process invoked by Valgrind tool to compress and index trace
    data
query/
    Query agent accepting JSON queries and processing them from the
    trace database
base/
    Core code shared by indexer and query
tests/
    Automated tests
scripts/
    Useful scripts

Licensing
=========

Valgrind is under the GPL. The Valgrind 'chronicle' tool's main.c file
is also under the GPL. The tool's headers --- arch.h, log_stream.h, and
effects.h --- use an X11 license, so they can be included by anyone. The
Chronicle 'indexer' and 'query' components are GPLed. They rely on a
'base' component whose files have an X11 license (including a simple C
JSON library).

The intent is that the individual Chronicle components are GPLed but
since they run in separate processes communicating via clearly defined
interfaces, non-GPLed code can communicate with them. In particular,
debugger front ends can use any license.

Contact
=======
robert@ocallahan.org
