*******************
Substitution Cipher
*******************
	
Description
===========

The substitution cipher is deceptively easy. Messages are encrypted using a key which is created in advance. 
You make the key by changing the alphabet:

.. figure:: assets/substitution.png

Your goal is to turn your micro:bit into a machine that can encode messages using a substitution cipher. We
call the message to be encrypted *plain text* and the encrypted message *cipher text*. You will need to store the alphabet with the substition cipher in your program. 
You can use a python dictionary to do this. A python dictionary for the substitution cipher above looks like this::

	key =  {'A':'V', 
		'B':'J', 
		'C':'Z', 
		'D':'B',
		  ...   }

Try encrypting and decrypting messages of your own and if you feel up to the challenge, try to decrypt the text below. 

	O zay vcur xzfyozx fr nb gorfuj rdfr lftm rcttat ydokd youu zcgct ucfgc nc rouu O, raa, fn fr tcjr; “fkkolczrfuub” at ardctyojc. Pctjpflozx rdc yolay rdfr nb kazzchoaz 
	yord dct dpjefzl’j “rckdzokfu nfrrctj” yfj jpvvokoczr ra czroruc nc ra doj nfzpjktowr, O eatc rdc lakpnczr fyfb fzl ecxfz ra tcfl or az rdc Uazlaz eafr. Or yfj f jonwuc, 
	tfneuozx rdozx—f zfogc jfouat’j cvvatr fr f wajr-vfkra loftb—fzl jrtagc ra tckfuu lfb eb lfb rdfr ufjr fyvpu gabfxc. O kfzzar frrcnwr ra rtfzjktoec or gctefron oz fuu 
	orj kuaplozcjj fzl tclpzlfzkc, epr O youu rcuu orj xojr czapxd ra jdcy ydb rdc japzl av rdc yfrct fxfozjr rdc gcjjcu’j jolcj eckfnc ja pzczlptfeuc ra nc rdfr O jrawwcl 
	nb cftj yord karraz. Qadfzjcz, rdfzm xal, lol zar mzay iporc fuu, cgcz rdapxd dc jfy rdc korb fzl rdc Rdozx, epr o jdfuu zcgct juccw kfunub fxfoz ydcz O rdozm av rdc 
	dattatj rdfr uptm kcfjcucjjub ecdozl uovc oz ronc fzl oz jwfkc, fzl av rdajc pzdfuuaycl eufjwdcnocj vtan culct jrftj ydokd ltcfn eczcfrd rdc jcf, mzayz fzl vfgaptcl 
	eb f zoxdrnftc kpur tcflb fzl cfxct ra uaajc rdcn az rdc yatul ydczcgct fzardct cftrdipfmc jdfuu dcfgc rdcot nazjrtapj jrazc korb fxfoz ra rdc jpz fzl fot.

	-- d.w. uagcktfvr, kfuu av krdpudp