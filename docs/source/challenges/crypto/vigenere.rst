****************
Vigenère Cipher
****************

This cipher, also called 'le chiffre indéchiffrable', was first described by Giovan Battista Belazzo. Although the concept is easy to understand, the cipher resisted 
breaking for three centuries, until Friedrich Kasiski introduced a succesful general attack.  

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

You can try to encipher and decipher your own messages. If you're up for a challenge, try to find the key and decrypt this ciphertext enciphered using Vigenère cipher:    

    Wckl'g jwym avr tlvfqydnxkwn vyehqgxat oof im lhm nqmna oyrmavz. vi  qtfg gwym  hzpdfhs  wf  p  ahschgjxzg  idjtawyt  jbxivs  dhyars  zr  avr  ucktsaiympca  dd  lbungq  
    tur  naqh  ucgtq  bag  vcrhewpprbuu  rudxjh  bc  axyhnxl  vhfodl-­‐uhgrs  jbms  sdpfz.

    Ifx  owgrfapyrg'q  zbwqt  rh avr  vyehll  pjlv  arcrbvbf  pjvvvba.  Gm  zolh  
    rahh  gwc  ulgg  spbuy  vc  cqpggtlvl  wf  ifx  woa  vyehqgxa  zhftac  usofick.  ph  fpwl  avni  ral  ssucva  cs  p  ntu  unayvawp  vyknzr  qjtzhrg  gl  swxt  ftcwav  
    whbf  ogybug  fbylosq  dsm  im  n  hjbjs  bu  jxtca  lptwdrs  phbbq  p  jtyur  vmek  pexad.  Avr  vsbks  naqh  asyaq  rvi  bc  uapqu  ejtusgh  ral  prhr  ihb  tpjtjhvr  
    etyuyt  zehggtpl  hfr  bgqlr,  udu  fbqu  nmn  joa  tvilqg  im  ihm  sdp  hus  ncb  poog  kmebbgppr  vftplbgogxmgz  skxqm  ac  utji  fch  gcahpvagmhhr  pdmlfjppwz.

    Ifx  owgrfapyrg'q  zbwqt  rh  avr  vyehll  hcesg  epralf  otrmlf  gwyg  avr  tlvfqydnxkwn  vyehqgxat. 
        
    
    -- Smnnznh Ywhaf, Wgmjvuxixy'g Txswl Hb Ifx Noypvr
