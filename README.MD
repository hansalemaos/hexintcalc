# Some functions to do mathematical operations on int/hex (automatic conversion of input dtypes - returns hex)

### Input formats: 
Here are some variations you can pass to the functions:

```python
"0x00000000`00000003"
"0x00000003"
"00000000`00000003"
"00000003"
"3"
"0x3"
3
3.0 (float will be converted to int)
```


```python
from hexintcalc import (
    hadd,
    hbitwiseand,
    hdivide,
    heq,
    hge,
    hgt,
    hexcalc,
    hle,
    hlshift,
    hlt,
    hmod,
    hmul,
    hne,
    number_to_hex,
    number_to_int,
    hor_,
    hpow,
    hrshift,
    hsub,
    hxor,
)
n1=hadd(n1=50,n2='0xf',zfill=0, backtick=True, add0x=True)
print(n1, int(n1.replace("`", ""), base=16))
n1=hdivide(n1=50,n2='0xf',zfill=0, backtick=True, add0x=True)
print(n1, int(n1.replace("`", ""), base=16))
n1=hbitwiseand(n1=50,n2='0xf',zfill=8, backtick=False, add0x=False)
print(n1, int(n1.replace("`", ""), base=16))
n1=hxor(n1=50,n2=100,zfill=0, backtick=False, add0x=True)
print(n1, int(n1.replace("`", ""), base=16))
n1=hor_(n1=50,n2='0xf',zfill=0, backtick=True, add0x=False)
print(n1, int(n1.replace("`", ""), base=16))
n1=hpow(n1=50,n2='a',zfill=0, backtick=False, add0x=False)
print(n1, int(n1.replace("`", ""), base=16))
n1=hlshift(n1=50,n2='0xf',zfill=0, backtick=True, add0x=False)
print(n1, int(n1.replace("`", ""), base=16))
n1=hmod(n1=50,n2='0xf',zfill=0, backtick=False, add0x=False)
print(n1, int(n1.replace("`", ""), base=16))
n1=hmul(n1=50,n2='0xf',zfill=0, backtick=False, add0x=True)
print(n1, int(n1.replace("`", ""), base=16))
n1=hrshift(n1=50,n2='0xf',zfill=0, backtick=True, add0x=False)
print(n1, int(n1.replace("`", ""), base=16))
n1=hsub(n1=50,n2='0xf',zfill=0, backtick=True, add0x=False)
print(n1, int(n1.replace("`", ""), base=16))
n1=hlt(n1=50,n2='0xf',zfill=0, backtick=False, add0x=True)
print(n1, int(n1.replace("`", ""), base=16))
n1=hle(n1=50,n2='0xf',zfill=0, backtick=False, add0x=False)
print(n1, int(n1.replace("`", ""), base=16))
n1=heq(n1=50,n2='0xf',zfill=0, backtick=False, add0x=False)
print(n1, int(n1.replace("`", ""), base=16))
n1=hne(n1=50,n2='0xf',zfill=0, backtick=False, add0x=True)
print(n1, int(n1.replace("`", ""), base=16))
n1=hge(n1=50,n2='0xf',zfill=0, backtick=False, add0x=False)
print(n1, int(n1.replace("`", ""), base=16))
n1=hgt(n1=50,n2='0xf',zfill=0, backtick=False, add0x=False)
print(n1, int(n1.replace("`", ""), base=16))


0x00000000`00000041 65
0x00000000`00000003 3
00000002 2
0x56 86
00000000`0000003f 63
15af1d78b58c400 97656250000000000
00000000`00190000 1638400
5 5
0x2ee 750
00000000`00000000 0
00000000`00000023 35
0x0 0
0 0
0 0
0x1 1
1 1
1 1


number_to_int('ff')
Out[9]: 255

number_to_hex(512)
Out[7]: '0x200'

```