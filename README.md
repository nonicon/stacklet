# Stacklet

[![make.fun · tiny-stack-vm-01-run-20261122](https://make.fun/badge/tiny-stack-vm-01-run-20261122.svg)](https://make.fun/bounty/tiny-stack-vm-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=tiny-stack-vm-01-run-20261122)
[![rank](https://make.fun/badge/tiny-stack-vm-01-run-20261122/nonicon/stacklet/rank.svg)](https://make.fun/bounty/tiny-stack-vm-01-run-20261122/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-stack-vm-01-run-20261122)
[![reward](https://make.fun/badge/tiny-stack-vm-01-run-20261122/nonicon/stacklet/reward.svg)](https://make.fun/bounty/tiny-stack-vm-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=tiny-stack-vm-01-run-20261122)

A tiny stack virtual machine for make.fun's tiny-stack-vm-01 ISA: 32-bit wrapping
integers, a 256-value stack, branches, calls, 256 words of memory, input/output,
and all ten traps with their exact exit codes. A faithful port of the kit's
reference VM — every hard rule (wrapping `MUL`, `INT_MIN / -1`, unsigned
`DIVU`/`MODU`/`LTU`, shift masking, `PUSH8` sign extension, step and output
limits, falling off the end) implemented exactly as specified.

`main.ts` (Node 22) runs all 40 programs of a set in one run, writing each
instance's `stdout.bin` and `exit.txt` under `/output/<id>/`.
