# nimord_code_task

This homework is a coding task of a small tool in Python 3,
and the second part is about testing your coding task on different platforms.

 

Coding task
----------------------

Implement a script in Python that searches one or more named input files
For lines containing a match to a regular expression pattern (given on the command line as well).
Assume that input is ascii, you don't need to deal with a different encoding.
If a line matches, print it. Please print the file name and the line number for every match.

Script accepts list optional parameters which are mutually exclusive:
-c ( --color ) which highlight matching text [1]
-m ( --machine ) which generate machine-readable output
format: file_name:no_line:start_pos:matched_text

Multiple matches on a single line are allowed, without overlapping.
The script should be compatible with Python3, and in line with PEP8 coding guidelines.
Add a few automated functional tests to your script (testing framework of your choice).

Hints:
* It is recommended to use a module for parsing the command line
arguments and the "re" module for matching the pattern.
* Try to use OOP in order to encapsulate differences between output formats.
If you do, please mention it in your documentation.

 

[1] http://www.pixelbeat.org/docs/terminal_colours

 

Testing with Python 3
---------------------------------------

In this part, you will reuse your tests written in the previous task.
As mentioned before you can use whatever testing framework you like.
We want to be able to run these tests on any system, do not assume any tools are installed, nor `virtualenv` availability

 

The only available tools on the system are:
- bash
- make
- docker


Docker service is configured and running.
The System is able to reach the public docker registry (hub.docker.com).
We want to run the tests on a python 3.7 container.
We expect that you provide a Makefile, which implements:
target 'build` to build the container for tests
target `run` to run the tests inside the container

HINT: Consider the container as a developer’s environment where you can repetitively test your script Which is under development. So you don't want to embed your script inside the container during the build.
