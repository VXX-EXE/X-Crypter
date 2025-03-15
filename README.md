# X Crypter 

## Crypter, binder

## Features 

Multiple files can be compiled into the stub. A file can either be embedded within the compiled executable, or the stub downloads the file at runtime.

Typically, an executable is decrypted and executed in-memory by the stub. If the executable is a native PE file, `RunPE` (process hollowing) is used. For .NET executables, the .NET stub uses `Invoke`. Legitimate files with no known signatures can be written to the disk.

## Obfuscation

Assembly code is obfuscated by nop-like instructions intermingled with the actual code, such as an increment followed by a decrement. Strings are not stored in the data section, but instead constructed on the stack using mov-opcodes.

The C# obfuscator replaces symbol names with barely distinguishable Unicode characters. Both string and integer literals are decrypted at runtime.

## Audience

In order to use this program, you should:

* be familiar with crypters and the basic concept of what a crypter does
* have a basic understanding of in-memory execution and evasion techniques
* acknowledge that uploading the stub to VirusTotal will decrease the time that the stub remains FUD

## FUD

This project is FUD on the day of release (March 2025). A crypter that is free, publicly available, and open source will not remain undetected for a long time. Adjusting the stub so it does not get detected is a daunting task and all efforts are in vain several days later. Therefore, there will be **no updates** to fix detection issues.

Rather, PEunion offers a fully functional implementation that is easy to modify and extend. If you want PEunion to be FUD, please get familiar with the code of the stub and adjust it until you are satisfied with the result.

However, additional evasion techniques may be implemented in future releases to improve the baseline design.

I do not take any responsibility for anybody who uses PEunion in illegal malware campaigns. This is an educational project.
