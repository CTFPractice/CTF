Training: Baconian
===
Hint: Baconian Cipher

先將大寫字母全部換成`B`，小寫字母全部換成`A`。五個一組放入list。
```python=
# bacon.py
ciphertext = "BaCoN's cIphEr or THE bacOnIAN CiPHer iS a meThOD oF sTEGaNOGrapHY (a METhoD Of HidIng A sECRet MeSsaGe as OpPOsEd TO a TRUe CiPHeR) dEVIseD BY francis bAcoN. a MessAge Is coNCeALED in THe pRESenTatIoN OF TexT, ratHer thaN iTs coNteNt. tO enCODe A MEsSaGe, eaCh lETter Of THe pLAInText Is rePLAcED By A groUp oF fIvE OF the letteRs 'A' or 'b'. ThIS ReplacemeNt Is DONe acCorDing TO the AlphaBet Of tHe BACOnIAN cIpHeR, sHoWn bElOw. NoTe: A SeCoNd vErSiOn oF BaCoN'S CiPhEr uSeS A UnIqUe cOdE FoR EaCh lEtTeR. iN OtHeR WoRdS, i aNd j eAcH HaS ItS OwN PaTtErN. tHe wRiTeR MuSt mAkE UsE Of tWo dIfFeReNt tYpEfAcEs fOr tHiS CiPhEr. AfTeR PrEpArInG A FaLsE MeSsAgE WiTh tHe sAmE NuMbEr oF LeTtErS As aLl oF ThE As aNd bS In tHe rEaL, sEcReT MeSsAgE, tWo tYpEfAcEs aRe cHoSeN, oNe tO RePrEsEnT As aNd tHe oThEr bS. tHeN EaCh lEtTeR Of tHe fAlSe mEsSaGe mUsT Be pReSeNtEd iN ThE ApPrOpRiAtE TyPeFaCe, AcCoRdInG To wHeThEr iT StAnDs fOr aN A Or a b. To dEcOdE ThE MeSsAgE, tHe rEvErSe mEtHoD Is aPpLiEd. EaCh 'TyPeFaCe 1' LeTtEr iN ThE FaLsE MeSsAgE Is rEpLaCeD WiTh aN A AnD EaCh 'TyPeFaCe 2' LeTtEr iS RePlAcEd wItH A B. tHe bAcOnIaN AlPhAbEt iS ThEn uSeD To rEcOvEr tHe oRiGiNaL MeSsAgE. aNy mEtHoD Of wRiTiNg tHe mEsSaGe tHaT AlLoWs tWo dIsTiNcT RePrEsEnTaTiOnS FoR EaCh cHaRaCtEr cAn bE UsEd fOr tHe bAcOn cIpHeR. bAcOn hImSeLf pRePaReD A BiLiTeRaL AlPhAbEt[2] FoR HaNdWrItTeN CaPiTaL AnD SmAlL LeTtErS WiTh eAcH HaViNg tWo aLtErNaTiVe fOrMs, OnE To bE UsEd aS A AnD ThE OtHeR As b. ThIs wAs pUbLiShEd aS An iLlUsTrAtEd pLaTe iN HiS De aUgMeNtIs sCiEnTiArUm (ThE AdVaNcEmEnT Of lEaRnInG). BeCaUsE AnY MeSsAgE Of tHe rIgHt lEnGtH CaN Be uSeD To cArRy tHe eNcOdInG, tHe sEcReT MeSsAgE Is eFfEcTiVeLy hIdDeN In pLaIn sIgHt. ThE FaLsE MeSsAgE CaN Be oN AnY ToPiC AnD ThUs cAn dIsTrAcT A PeRsOn sEeKiNg tO FiNd tHe rEaL MeSsAgE."
bacon = ""
count = 0
lis = []

for i in ciphertext:
	if (count%5==0):
		if len(bacon)==5:
			lis.append(bacon)
		bacon=''
	if (ord(i)>=65 and ord(i)<=90):
		count+=1
		bacon+='B'
	elif (ord(i)>=97 and ord(i)<=122):
		count+=1
		bacon+='A'
	else:
		pass
```

將培根密碼解密。
```python=
text = ""

for i in lis:
	if i=='AAAAA':
		text+='a'
	elif i=='AAAAB':
		text+='b'
	elif i=='AAABA':
		text+='c'
	elif i=='AAABB':
		text+='d'
	elif i=='AABAA':
		text+='e'
	elif i=='AABAB':
		text+='f'
	elif i=='AABBA':
		text+='g'
	elif i=='AABBB':
		text+='h'
	elif i=='ABAAA':
		text+='i'
	elif i=='ABAAB':
		text+='j'
	elif i=='ABABA':
		text+='k'
	elif i=='ABABB':
		text+='l'
	elif i=='ABBAA':
		text+='m'
	elif i=='ABBAB':
		text+='n'
	elif i=='ABBBA':
		text+='o'
	elif i=='ABBBB':
		text+='p'
	elif i=='BAAAA':
		text+='q'
	elif i=='BAAAB':
		text+='r'
	elif i=='BAAAB':
		text+='s'
	elif i=='BAABB':
		text+='t'
	elif i=='BABAA':
		text+='u'
	elif i=='BABAB':
		text+='v'
	elif i=='BABBA':
		text+='w'
	elif i=='BABBB':
		text+='x'
	elif i=='BBAAA':
		text+='y'
	elif i=='BBAAB':
		text+='z'
	else:
		pass
```

將字母`x`的位置以空白取代。
```python=
for i in text:
	if(i=='x'):
		print(' ', end="")
	else:
		print(i, end="")
```

把程式run起來就能拿到keyword了。

![](https://i.imgur.com/aPox8O1.png)