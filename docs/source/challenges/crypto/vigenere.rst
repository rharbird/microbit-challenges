****************
Vigenère Cipher
****************

This cipher, also called 'le chiffre indéchiffrable', was first described by Giovan Battista Belazzo. Although the concept is easy to understand, the cipher resisted 
breaking for three centuries until Friedrich Kasiski introduced a first succesful general attack.  

.. figure:: assets/vigenere_table.jpg
   :align: center
   
   Vigenère table (Source: https://tinyurl.com/yxmbt48f)

It works similarly to Caesar substitution cipher, since it's also based on shifting aplhabet positions. This time instead of shifting all letters 
by the same value, we choose a keyword which determines a different value for each letter in the plaintext.

As an example, suppose that this is our plaintext: ::
    
    ATTACKATDAWN

Then you choose a keyword (such as snake) and repeat it for each row of plaintext: ::

    SNAKESNAKESN

Then you use each letter of the key to determine the shift of every letter of the plaintext: ::

    Plaintext:  ATTACKATDAWN
    Key:        SNAKESNAKESN
    Ciphertext: SGTKGCNTNEOA

You can try to encipher and decipher your own messages. If you're up for a challenge, try to find the key and decrypt this ciphertext enciphered using Vigenère cipher (hint:
it's not easy):    

    Wckl'g jwym avr Tlvfqydnxkwn Vyehqgxat oof im lhm nqmna oyrmavz. Vi  qtfg gwym  hzpdfhs  wf  p  ahschgjxzg  idjtawyt  jbxivs  dhyars  zr  avr  ucktsaiympca  dd  lbungq  
    tur  naqh  ucgtq  bag  vcrhewpprbuu  rudxjh  bc  axyhnxl  vhfodl-­‐uhgrs  jbms  sdpfz.

    Hut  Fbaquwgdlf'f  Vsbks  Gd Ral Unayqf  oyhm  flbgxmgz  oyrmavz.  Vi  qtfg  gwym  avr  qcla  rexld  pb  rmglasarc  bz  hut  ntu  unayvawp  vyknzr  qjtzhrg.  Gm  
    zolh  rahh  gwc  xmtrrr  hm  o  cpl  zhznrrbj  ungeel  pypqmlf  vh  jbrs  uptbuu  ldsk  ifnxll  zanhfxk  chi  zr  h  gyxax  vt  ytkhu  kepnilr  edsgk  o  yppzl  
    ubab  uywpz.  Ral  uhxbx  hzfd  rxszf  nmn  vb  jwgvo  dyplxag  gwc  ulgg  eyg  noypampq  tppzss  oaylaseh  ykl  avmcw,  ocj  bsvo  mbj  atu  skecva  hb  eyr  mce  
    dlx  hbq  lfta  jbasgaoen  mknoaxxtawbcq  xewfi  rh  osye  whb  frwyupzviyml  osickdoesq.

    Mos  Uxrvovvzck'z  Uhxbx  Ac  Gwc  Zhznmw  llzyh  ptavrg  zxahrg  rahb  gwc  Xuqlrjhwsqxy  Zhznrrbjo.
        
    
    -- Smnnznh Ywhaf, Wgmjvuxixy'g Txswl Hb Ifx Noypvr