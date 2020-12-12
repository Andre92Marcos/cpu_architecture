Functions are called using the call instruction. Call pushes the return address to the stack when called

The first 6 function parameters are passed through registers (in a 64bit) RDI, RSI, RDX, RCX, R8 and R9. After this the parameters are passed through the stack. Large parameters/structures passed by value are passed through the stack.

ret is used to return from a function. The return address is popped oof the stack and placed into the RIP.

Since the first 6 paramenters are passed through the registers, before a function is called it may be required to save the values already in the parameters into the stack, so that they are not overriden by the function arguments.

So when calling a function:
	1st) We ssave the values already existing in the registers to the stack
	2nd) We move the arguements of the function to the registers.
	3rd) When call is executed it pushes the return address (next instruction to be executed) to the stack and the RIP points to it.

So when a function starts (so it has just been called):

	1st) The RBP is pushed to the stack (push rbp)
	2nd) The RSP points to the RBP. (mov rbp,rsp)
	3rd) Grap the function arguments from the registers to the stack

At the end of a function:
	1st) We pop RBP;
	2nd) We ues ret;
