# Unskilled vim commands

## how to move cursor
 * Ctrl + F/B
 * Ctrl + D/U
 * H, M, L

 * space/ backspace,   good move!
 * Enter = next line = j
 * 0, used very seldom
 * 66G  -- goto line 66
 * 3S   -- delete 3 lines and insert
 * 6cw  -- remove 6 words and insert

## how to delete and insert
 * dw/diw/daw : remove a word
 * cw/ciw/caw : remove a word and insert here
 
    ** best practice: daw/ciw works best.  das/dap;  cis/cip.**

 * #/*        : find WordPress
 * f/t/F/T       : t means till / souds only work for current line unde^r ATOM
 * /          : / works for searching ... under ATOM; /+n+N works!!!
 * Ctrl + w   : delete a word / insert mode
 * Ctrl + u   : remove all till line Beginning(0) / insert mode

 * C          : remove all till end of this line;
 * difference of 0 ^ $ ; when commenting a block, try 0 instead of ^, which looks better
 * if a whole line does not make any sense, just remove it and input new jobs; two ways:
  - 1 ddo
  - 2 S/cc

##  VERY important
 * all :commands doesnot work under ATOM, such as :%s/going/rolling/g DOESn't WORK!!!
 * all / commands  works under ATOM
 * Strategy for choice: 扬长避短 try to make most of VIM 's strength and avoid using its weakness. Use ATOM instead when VIM is inconvenient.

## Undo & Redo
 * Cmd + Z/ Cmd + Y
 * u / Ctrl-r
