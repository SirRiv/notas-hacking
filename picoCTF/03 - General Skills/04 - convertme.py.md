## Descripción

Run the Python script and convert the given number from decimal to binary to get the flag.[Download Python script](https://artifacts.picoctf.net/c/24/convertme.py)

Hints:
1. Look up a decimal to binary number conversion app on the web or use your computer's calculator!
2. The `str_xor` function does not need to be reverse engineered for this challenge.
3. If you have Python on your computer, you can download the script normally and run it. Otherwise, use the `wget` command in the webshell.
4. To use `wget` in the webshell, first right click on the download link and select 'Copy Link' or 'Copy Link Address'
5. Type everything after the dollar sign in the webshell: `$ wget` , then paste the link after the space after `wget` and press enter. This will download the script for you in the webshell so you can run it!
6. Finally, to run the script, type everything after the dollar sign and then press enter: `$ python3 convertme.py`

## Solución 

Usamos CyberChef

```
SrRiv-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/24/convertme.py
--2025-03-17 02:11:47--  https://artifacts.picoctf.net/c/24/convertme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.16, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1189 (1.2K) [application/octet-stream]
Saving to: 'convertme.py'

convertme.py                                   100%[====================================================================================================>]   1.16K  --.-KB/s    in 0.001s  

2025-03-17 02:11:47 (1.79 MB/s) - 'convertme.py' saved [1189/1189]

SrRiv-picoctf@webshell:~$ python convertme.py
If 55 is in decimal base, what is it in binary base?

Input:55
Recipe: To Binary
Output: 00110101 00110101

Answer: 00110101 00110101
That isn't a binary number. Binary numbers contain only 1's and 0's
SrRiv-picoctf@webshell:~$ python convertme.py
If 47 is in decimal base, what is it in binary base?

Input: 47
Recipe: From Decimal, To Binary
Output: 00101111

Answer: 00101111
That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_722f6b39}
SrRiv-picoctf@webshell:~$

picoCTF{4ll_y0ur_b4535_722f6b39}
```
## Notas adicionales 
## Referencias