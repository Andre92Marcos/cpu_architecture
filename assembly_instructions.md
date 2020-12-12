**ret - return**

	The ret instruction transfers control to the return address located on the stack. This address is usually placed on the stack by a call instruction. Issue the ret instruction within the called procedure to resume execution flow at the instruction following the call.

**LEA - Load Effective Address**
	Loads the address of the memory calcutlation into the register.
	Does not dereference the value as MOV would
	Used for example to save arrays
