## Descripción
We made a lot of substitutions to encrypt this. Can you decrypt it? Connect with `nc jupiter.challenges.picoctf.org 13758`.
## Solución
El servidor tenía el siguiente texto:
```
-------------------------------------------------------------------------------
tnecoxbs qkok is dnzo vhxc - voklzketd_is_t_nwko_hxfpax_aewbvobxdz
-------------------------------------------------------------------------------
qxwiec qxa snfk bifk xb fd aismnsxh yqke ie hneane, i qxa wisibka bqk poibisq fzskzf, xea fxak skxotq xfnec bqk pnnjs xea fxms ie bqk hipoxod okcxoaiec boxesdhwxeix; ib qxa sboztj fk bqxb snfk vnokjenyhkack nv bqk tnzebod tnzha qxoahd vxih bn qxwk snfk ifmnobxetk ie akxhiec yibq x enphkfxe nv bqxb tnzebod. i viea bqxb bqk aisboitb qk exfka is ie bqk krbokfk kxsb nv bqk tnzebod, gzsb ne bqk pnoakos nv bqokk sbxbks, boxesdhwxeix, fnhaxwix xea pzjnwiex, ie bqk fiasb nv bqk txomxbqixe fnzebxies; nek nv bqk yihaksb xea hkxsb jenye mnobines nv kzonmk. i yxs enb xphk bn hicqb ne xed fxm no ynoj ciwiec bqk krxtb hntxhibd nv bqk txsbhk aoxtzhx, xs bqkok xok en fxms nv bqis tnzebod xs dkb bn tnfmxok yibq nzo nye noaexetk szowkd fxms; pzb i vnzea bqxb pisboibu, bqk mnsb bnye exfka pd tnzeb aoxtzhx, is x vxiohd ykhh-jenye mhxtk. i sqxhh kebko qkok snfk nv fd enbks, xs bqkd fxd okvoksq fd fkfnod yqke i bxhj nwko fd boxwkhs yibq fiex.

```
usando la página gullaba.de y la herramienta substitution-solver obtuve el texto:
```
-------------------------------------------------------------------------------
congrats here is your flag - frequency_is_c_over_lambda_dnvtfrtayu
-------------------------------------------------------------------------------
having had some time at my disposal when in london, i had visited the british museum, and made search among the books and maps in the library regarding transylvania; it had struck me that some foreknowledge of the country could hardly fail to have some importance in dealing with a nobleman of that country. i find that the district he named is in the extreme east of the country, just on the borders of three states, transylvania, moldavia and bukovina, in the midst of the carpathian mountains; one of the wildest and least known portions of europe. i was not able to light on any map or work giving the exact locality of the castle dracula, as there are no maps of this country as yet to compare with our own ordnance survey maps; but i found that bistritz, the post town named by count dracula, is a fairly well-known place. i shall enter here some of my notes, as they may refresh my memory when i talk over my travels with mina.
```
que contiene la llave:
```
frequency_is_c_over_lambda_dnvtfrtayu
```
Ya que la pista del reto me dice que la llave no está en el formato original
## Notas
## Referencias
https://www.guballa.de/substitution-solver