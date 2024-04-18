## Objetivo

In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/3cfeb09681369c26e3f19d886bc1e5d9/values)
## Datos de acceso
## Solución

Utilizamos un programa en Java que realiza todo el proceso y para sacar phi utilizamos una web que obtiene el numero Eulers Totient

obteniendo la bandera


```
PS C:\Users\czarr\Desktop> java RSA.java
Insert N
769457290801263793712740792519696786147248001937382943813345728685422050738403253
Input e
65537
Input c
8533139361076999596208540806559574687666062896040360148742851107661304651861689
Input phi
769457290801263793712740792519696786146770691257482771401340787987731866151331520
d = 582402748221564772374696843202153883711652351188297188998024166320268538694734273
m = 13016382529449106065927291425342535437996222135352905256639629442503647501498237
m in base 256 = [125, 55, 56, 51, 57, 54, 51, 53, 52, 95, 100, 111, 48, 103, 95, 48, 110, 95, 78, 95, 49, 49, 97, 109, 115, 123, 70, 84, 67, 111, 99, 105, 112]
Convert with ASCII
}78396354_do0g_0n_N_11ams{FTCocip
PS C:\Users\czarr\Desktop>
```

```
picoCTF{sma11_N_n0_g0od_45369387}
```
## Notas adicionales 

## Referencias