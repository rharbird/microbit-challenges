*******************
Substitution Cipher
*******************
	
Description
===========

The substitution cipher is deceptively easy. Messages are encrypted using a key which is created in advance. 
You make the key by changing positions of letters in the alphabet:

.. figure:: assets/substitution.png

To be able to encode and decode messages using a substitution cipher, you will need to create your the key used to generate ciphertext and store it. A dictionary might 
be a good data structure for this purpose.
A Python dictionary for the substitution cipher above would look something like this::

	key =  {'A':'V', 
		'B':'J', 
		'C':'Z', 
		'D':'B',
		  ...   }

Try encrypting and decrypting messages of your own and if you feel up to the challenge, try to decrypt the text below. To save you the effort, the key above does not 
apply to the message. Try to think of (or look for) language properties or techniques that could help you find the key. 

	O zay vcur xzfyozx fr nb gorfuj rdfr lftm rcttat ydokd youu zcgct ucfgc nc rouu O, raa, fn fr tcjr; “fkkolczrfuub” at ardctyojc. Pctjpflozx rdc yolay rdfr nb kazzchoaz 
	yord dct dpjefzl’j “rckdzokfu nfrrctj” yfj jpvvokoczr ra czroruc nc ra doj nfzpjktowr, O eatc rdc lakpnczr fyfb fzl ecxfz ra tcfl or az rdc Uazlaz eafr. Or yfj f jonwuc, 
	tfneuozx rdozx—f zfogc jfouat’j cvvatr fr f wajr-vfkra loftb—fzl jrtagc ra tckfuu lfb eb lfb rdfr ufjr fyvpu gabfxc. O kfzzar frrcnwr ra rtfzjktoec or gctefron oz fuu 
	orj kuaplozcjj fzl tclpzlfzkc, epr O youu rcuu orj xojr czapxd ra jdcy ydb rdc japzl av rdc yfrct fxfozjr rdc gcjjcu’j jolcj eckfnc ja pzczlptfeuc ra nc rdfr O jrawwcl 
	nb cftj yord karraz. Qadfzjcz, rdfzm xal, lol zar mzay iporc fuu, cgcz rdapxd dc jfy rdc korb fzl rdc Rdozx, epr o jdfuu zcgct juccw kfunub fxfoz ydcz O rdozm av rdc 
	dattatj rdfr uptm kcfjcucjjub ecdozl uovc oz ronc fzl oz jwfkc, fzl av rdajc pzdfuuaycl eufjwdcnocj vtan culct jrftj ydokd ltcfn eczcfrd rdc jcf, mzayz fzl vfgaptcl 
	eb f zoxdrnftc kpur tcflb fzl cfxct ra uaajc rdcn az rdc yatul ydczcgct fzardct cftrdipfmc jdfuu dcfgc rdcot nazjrtapj jrazc korb fxfoz ra rdc jpz fzl fot.

	-- D.W. Uagcktfvr, Kfuu Av Krdpudp