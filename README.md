# PetitPotam
PoC tool to coerce Windows hosts to authenticate to other machines via MS-ESFRPC EfsRpcOpenFileRaw function. This is possible via other protocols and functions as well ;) .

The tools use the LSARPC named pipe with inteface c681d488-d850-11d0-8c52-00c04fd90f7e because it's more prevalent.

But it's possible to trigger with the EFSRPC named pipe and interface df1941c5-fe89-4e79-bf10-463657acf44d. 

Disabling the EFS service seems not to mitigate the "feature".

The Python one require Impacket to be installed, the Windows PoC was done on VS 2019 Community.
If compilation problem, remember to add Rpcrt4.lib in the linker. Compile in x86.

Inspired by the previous work on MS-RPRN from @tifkin_ & @elad_shamir and others SpecterOps guys.

MS-EFSRPC - Encrypting File System Remote (EFSRPC) Protocol

https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-efsr/08796ba8-01c8-4872-9221-1000ec2eff31
