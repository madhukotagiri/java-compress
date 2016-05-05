## Aim ##
  * Provide strategy based API for choosing various java based compression algorithms
  * Provide (selectively) pure java implementation of compression algo.

## Why GPL ##
LZO is released under GPL, so the derivative code license needs to be also GPL.
In future, need to see how to include various helpers (with different license schemes) -- IANAL

## Why lots of switch-case statements and complex code flow ##
Original code is taken from minilzo.c (version 2.03 http://www.oberhumer.com/opensource/lzo/#minilzo ). The Java-code is translated from C-code. Original C-code uses _goto_ statements, which are not available in java. So _goto-statements_ are simulated using **while-loop** and **switch-case** statements.

## Why project name is java-compress ##
Ultimate aim is to provide more compression algorithm helper classes other than LZO

## What other algorithm's helpers are planned ##
  * [LZJB](http://src.opensolaris.org/source/xref/onnv/onnv-gate/usr/src/uts/common/fs/zfs/lzjb.c)
  * [FastLZ](http://www.fastlz.org)
  * [QuickLZ](http://www.quicklz.com)
  * etc