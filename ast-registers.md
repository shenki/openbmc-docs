# Registers on the AST2400

## AST vs OBMC

AST kernel was booted first. Using AST u-boot.

### All registers

|Register|AST Kernel  |OBMC Kernel |Comment
|--------|------------|------------|--------
| SCU 00 | `00000000` | `00000001` | SCU unlocked. We should lock the SCU, but this is okay for now
| SCU 04 | `ff0ea088` | `ff0ea088` |
| SCU 08 | `71b4b008` | `71b4b008` |
| SCU 0c | `10cc5e80` | `10cc5e80` |
| SCU 10 | `00000000` | `00000000` |
| SCU 14 | `00003fef` | `00003fef` |
| SCU 18 | `00000000` | `00000000` |
| SCU 1c | `00026108` | `00026108` |
| SCU 20 | `000003f1` | `000003f1` |
| SCU 24 | `00000291` | `00000291` |
| SCU 28 | `10141811` | `10141811` |
| SCU 2c | `00001010` | `00001010` |
| SCU 30 | `20001a03` | `20001a03` |
| SCU 34 | `20001a03` | `20001a03` |
| SCU 38 | `04000030` | `04000030` |
| SCU 3c | `00000001` | `00000003` | OBMC has watchdog reset flag enabled
| SCU 40 | `000000c1` | `000000c1` |
| SCU 44 | `00000010` | `00000010` |
| SCU 48 | `00002255` | `00002255` |
| SCU 4c | `00000023` | `00000023` |
| SCU 50 | `00000000` | `00000000` |
| SCU 54 | `00000000` | `00000000` |
| SCU 58 | `00000000` | `00000000` |
| SCU 5c | `fc3fffe2` | `fc3fffe2` |
| SCU 60 | `ffffdeea` | `ffffdeea` |
| SCU 64 | `ff7dfefe` | `ff7dfefe` |
| SCU 68 | `feefffff` | `feefffff` |
| SCU 6c | `10dbffff` | `10dbffff` |
| SCU 70 | `120ce406` | `120ce406` |
| SCU 74 | `0000000e` | `0000000e` |
| SCU 78 | `842fe534` | `22b1c27b` | Random number generator
| SCU 7c | `02010303` | `02010303` |
| SCU 80 | `cb000000` | `cb000000` |
| SCU 84 | `00fff0c0` | `00fff0c0` |
| SCU 88 | `01c000ff` | `c1c000ff` |OBMC has MAC#1 MDIO1 and MAC#1 MDC1 enabled. Unknown?
| SCU 8c | `c1c000ff` | `c1c000ff` |
| SCU 90 | `003fa009` | `003fa009` |
| SCU 94 | `00000000` | `00000000` |
| SCU 98 | `00000000` | `00000000` |
| SCU 9c | `001fdff3` | `001fdff3` |
| SCU a0 | `00000000` | `00000000` |
| SCU a4 | `ffff0000` | `ffff0000` |
| SCU a8 | `000fffff` | `000fffff` |
| SCU ac | `00000000` | `00000000` |
| SCU b0 | `00000000` | `00000000` |
| SCU b4 | `00000000` | `00000000` |
| SCU b8 | `00000000` | `00000000` |
| SCU bc | `00000000` | `00000000` |
| SCU c0 | `00000000` | `00000000` |
| SCU c4 | `00000000` | `00000000` |
| SCU c8 | `00000000` | `00000000` |
| SCU cc | `00000000` | `00000000` |
| SCU d0 | `00000001` | `00000001` |
| SCU d4 | `00000000` | `00000000` |
| SCU d8 | `00000000` | `00000000` |
| SCU dc | `00000000` | `00000000` |
| SCU e0 | `7f82d2f8` | `a44c1980` | Counter
| SCU e4 | `00000002` | `00000003` | Counter

### Changes

|Register|AST Kernel  |OBMC Kernel |Comment
|--------|------------|------------|--------
| SCU 00 | `00000000` | `00000001` |SCU unlockd. We should lock the SCU, but this is okay for now
| SCU 3c | `00000001` | `00000003` | OBMC has watchdog reset flag enabled
| SCU 78 | `842fe534` | `22b1c27b` | Random number generator
| SCU 88 | `01c000ff` | `c1c000ff` |OBMC has MAC#1 MDIO1 and MAC#1 MDC1 enabled. Unknown?
| SCU e0 | `7f82d2f8` | `a44c1980` | Counter
| SCU e4 | `00000002` | `00000003` | Counter
