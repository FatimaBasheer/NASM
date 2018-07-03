# NASM(Netwide Assembler)
---------------Executing a NASM program----------------
1. Assembling the source file
    $nasm -f elf filename.asm
#This creates an object file, filename.o in the current working directory.
2. Creating an executable file
------For a 32 bit machine-----
    $ld filename.o -o output filename
------For 64 bit machine
    $ld -melf i386 filename-----
#This creates an executable file of the name output filename.
3. Program execution
    $./output filename
#For example, if the program to be run is test.asm
  $nasm -f elf test.asm
  $ld test.o -o output
  $./output
