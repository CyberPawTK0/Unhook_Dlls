# Unhook_Dlls

The code being shared performs unhooking to all DLLs. The heavy lifting are done by the 2 functions below which are found in main.c.

if (InitializeNtSyscalls()) {
  UnhookAllLoadedDlls();
}

The code does not perform execution of the shellcode, but the way we did it to bypass MDE was after unhooking simply use IPv4 obfuscation (Using HellShell) along with APC Injection. 


Better understood if you known NTDLL Unhooking (KnownDLLs Director) and Indirect Syscalls (HellsHall)
