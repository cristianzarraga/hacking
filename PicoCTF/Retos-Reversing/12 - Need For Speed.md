## Objetivo

The name of the game is [speed](https://www.youtube.com/watch?v=8piqd2BWeGI). Are you quick enough to solve this problem and keep it above 50 mph? [need-for-speed](https://jupiter.challenges.picoctf.org/static/cd51b2c95be9f3626db6fe6665afb5a3/need-for-speed).
## Datos de acceso
## Solución


```
End of assembler dump.
(gdb) breakpoint (main+30)
Undefined command: "breakpoint".  Try "help".
(gdb) breakpoint *(main+30)
Undefined command: "breakpoint".  Try "help".
(gdb) break (main+30)      
Function "(main+30)" not defined.
Make breakpoint pending on future shared library load? (y or [n]) n
(gdb) 
Function "(main+30)" not defined.
Make breakpoint pending on future shared library load? (y or [n]) n
(gdb) break *(main+30)
Breakpoint 1 at 0x938
(gdb) run
Starting program: /home/czarragar-picoctf/need-for-speed 
warning: Error disabling address space randomization: Operation not permitted
[Thread debugging using libthread_db enabled]
Using host libthread_db library "/lib/x86_64-linux-gnu/libthread_db.so.1".
Keep this thing over 50 mph!
============================


Breakpoint 1, 0x0000558a89600938 in main ()
(gdb) jump *(main+35)
Continuing at 0x558a8960093d.
Creating key...
Finished
Printing flag:
PICOCTF{Good job keeping bus #24c43740 speeding along!}
[Inferior 1 (process 256) exited normally]
(gdb) 
```

```
PICOCTF{Good job keeping bus #24c43740 speeding along!}
```
## Notas adicionales 

## Referencias