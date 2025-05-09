## Descripción
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [this](https://mercury.picoctf.net/static/5ef2e9103d55972d975437f68175b9ab/dolls.jpg)
Hints:
1. Wait, you can hide files inside files? But how do you find them?
2. Make sure to submit the flag as picoCTF{XXXXX}


## Solución 

~~~
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/Matryoshka$ ls
dolls.jpg
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/Matryoshka$ unzip dolls.jpg
Archive:  dolls.jpg
warning [dolls.jpg]:  272492 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: base_images/2_c.jpg
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/Matryoshka$ unzip dolls.jpg
Archive:  dolls.jpg
warning [dolls.jpg]:  272492 extra bytes at beginning or within zipfile
  (attempting to process anyway)
replace base_images/2_c.jpg? [y]es, [n]o, [A]ll, [N]one, [r]ename: ^Csrriv@LAPTOP-7DDM83G8:~/SRSS/forensic/Matryoshka$
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/Matryoshka$ ls
base_images  dolls.jpg
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/Matryoshka$ cd base_images/
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/Matryoshka/base_images$ ls
2_c.jpg
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/Matryoshka/base_images$ unzip 2_c.jpg
Archive:  2_c.jpg
warning [2_c.jpg]:  187707 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: base_images/3_c.jpg
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/Matryoshka/base_images$ ls
2_c.jpg  base_images
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/Matryoshka/base_images$ cd base_images/
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/Matryoshka/base_images/base_images$ ls
3_c.jpg
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/Matryoshka/base_images/base_images$ unzip 3_c.jpg
Archive:  3_c.jpg
warning [3_c.jpg]:  123606 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: base_images/4_c.jpg
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/Matryoshka/base_images/base_images$ cd base_images/
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/Matryoshka/base_images/base_images/base_images$ ls
4_c.jpg
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/Matryoshka/base_images/base_images/base_images$ unzip 4_c.jpg
Archive:  4_c.jpg
warning [4_c.jpg]:  79578 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: flag.txt
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/Matryoshka/base_images/base_images/base_images$ ls
4_c.jpg  flag.txt
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/Matryoshka/base_images/base_images/base_images$ cat flag.txt
picoCTF{e3f378fe6c1ea7f6bc5ac2c3d6801c1f}
~~~

`picoCTF{e3f378fe6c1ea7f6bc5ac2c3d6801c1f}`
## Notas adicionales 

Al archivo .jpg se puede descomprimir con con unzip, gracias a binwalk nos dimos cuenta de eso, podemos seguir descomprimiendo hasta encontrar el archivo flag.txt
## Referencias
