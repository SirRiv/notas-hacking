## Descripción
#### Description

I've hidden a flag in this file. Can you find it? [Forensics is fun.pptm](https://mercury.picoctf.net/static/52da699e0f203321c7c90ab56ea912d8/Forensics%20is%20fun.pptm)
## Solución 

~~~
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/MacroHard$ ls
'Forensics is fun.pptm'  '[Content_Types].xml'   _rels   docProps   ppt
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/MacroHard$ cat ppt/slideMasters/hidden
Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Qsrriv@LAPTOP-7DDM83G8:~/SRSS/forensic/MacroHard$ cat ppt/slideMasters/hidden | tr -d ' '
ZmxhZzogcGljb0NURntEMWRfdV9rbjB3X3BwdHNfcl96MXA1fQsrriv@LAPTOP-7DDM83G8:~/SRSS/forensic/MacroHard$ cat ppt/slideMasters/hidden | tr -d ' ' | base64
Wm14aFp6b2djR2xqYjBOVVJudEVNV1JmZFY5cmJqQjNYM0J3ZEhOZmNsOTZNWEExZlE=
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/MacroHard$ cat ppt/slideMasters/hidden | tr -d ' ' | base64 -d
flag: picoCTF{D1d_u_kn0w_ppts_r_z1p5}base64: invalid input
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/MacroHard$
~~~

`picoCTF{D1d_u_kn0w_ppts_r_z1p5}`


## Notas adicionales 

Los archivos pptm son presentaciones powerpoint pero con los macros habilitados. Las presentaciones PowerPoint son archivos zip, por lo que podemos realizar un unzip, observamos un archivo  con la palabra `hidden` le hacemos cat y obtenemos la bandera decodificando de base 64. 
## Referencias
