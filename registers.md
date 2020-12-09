**register stack pointer - rsp**
	stores the address of the last program request in a stack
	the stack grows down im memory and the rsp points to the lowest occupied stack location (not the next one to use)

**register base pointer - rbp**
	points to the base of the current stack frame allocated to the routine;
	the stack frame stores the local variables and the parameters passed to the function

**register instruction pointer - rip**
	points to the next instruction to exectue

**register destination index - rdi**
	destination for data copies, used to pass the 1st argument to functions

**register source index - rsi**
	used to pass the 2nd argument to functions
