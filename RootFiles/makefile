# Define required macros here
REMOVE = rm
CC = gcc

# Explicit rules, all the commands you can call with make 
# (note: the <tab> in the command line is necessary for make to work) 
# target:  dependency1 dependency2 ...
#       <tab> command

# Called by: make targetname 
# Also executed when you just called make. This calls the first target. 
all: vulnerable_root_prog  setup 

vulnerable_root_prog: vulnerable_root_prog.c
	$(REMOVE) -rf ../Root/
	mkdir ../Root/
	$(CC) vulnerable_root_prog.c -o ../Root/vulnerable_root_prog

# refresh the root files and root log file
# Set UID for rootprog and rootdo
setup: 
	chmod u+s ../Root/vulnerable_root_prog 

clean:
	$(REMOVE) ../Root/vulnerable_root_prog
	$(REMOVE) -rf ../Root/