# assembly-64
x86-64+AVX2 assembly language 

to compile this code; run
```
gcc -mavx2 -c fizzbuzz.S
ld -o fizzbuzz fizzbuzz.o
```
to run this code, you will need to pipe it to cat

```
./fixxbuzz | cat

```
use taskset to force the programs onto particular CPUs: 

```
taskset 1 ./fizzbuzz | taskset 2 pv > /dev/null
```
