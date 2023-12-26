---
title: 'حلول الاختبار التأهيلي (المرحلة الثانوية)'
description: 'أذكى 2024 باللغتين: C++ وبايثون'
lang: ar
layout: athka
---
<div dir="auto">
  
# حلول الاختبار التأهيلي أذكى 2024


<h2>كتب هذا الملف:</h2>
<ul>
    <li>معاذ القرني</li>
    <li>يزن آشي</li>
</ul>

{%- include athka-tgchannel.html -%}

<table class="table table-bordered table-striped">
    <thead>
        <tr>
            <th>الاسم</th>
            <th>الدرجة</th>
            <th>هل تختلف المعطيات بين الطلاب؟</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>الجملة الشرطية  IF</td>
            <td>20</td>
            <td>نعم</td>
        </tr>
        <tr>
            <td>التكرار</td>
            <td>31</td>
            <td>نعم</td>
        </tr>
        <tr>
            <td>معادلة خالد</td>
            <td>37</td>
            <td>نعم</td>
        </tr>
        <tr>
            <td>الاستدعاء الذاتي لعبير</td>
            <td>40</td>
            <td>نعم</td>
        </tr>
        <tr>
            <td>واجب ريم المنزلي</td>
            <td>42</td>
            <td>نعم</td>
        </tr>
        <tr>
            <td>الأعداد الجيدة</td>
            <td>43</td>
            <td>نعم</td>
        </tr>
        <tr>
            <td>المجموعة الجزئية</td>
            <td>44</td>
            <td>لا</td>
        </tr>
    </tbody>
</table>

##  الجملة الشرطية IF 
**الفكرة:** ننسخ الكود ونضيف أمر طباعة للمتغير المطلوب
<details>
  <summary>الحل بلغة С++</summary>

```c++
#include <iostream>
using namespace std;
int main()
{
  int x = 11;
  int y = 29;
  int z;

  if (x % 2 != 0) {
    if (x > y) {
        z = 0;
    } else {
        z = 1;
    }
  } else {
    if (x > y) {
        z = 2;
    } else {
        z = 3;
    }
  }
  cout << z; // أضفنا أمر الطباعة
}
```

</details> 

<details>
  <summary>الحل بلغة بايثون</summary>
  
```py
x = 11
y = 29

if x % 2 != 0:
    if x > y:
        z = 0
    else:
        z = 1
else:
    if x > y:
        z = 2
    else:
        z = 3

print(z) # أضفنا أمر الطباعة
```

</details>

## التكرار
**الفكرة:** ننسخ الكود ونضيف أمر طباعة للمتغير المطلوب

<details>
  <summary>الحل بلغة C++</summary>

```c++
#include <iostream>
using namespace std;
int main()
{
  int r = 0;    
  for (int i = 0; i < 100; i++) {
  	r = (277 * r + 241) % 433;
  }
  cout << r; // أضفنا أمر الطباعة
}
```
  
</details>

<details>
  <summary>الحل بلغة بايثون</summary>

```py
r = 0
for i in range(100):
    r = (277 * r + 241) % 433
print(r) # أضفنا أمر الطباعة
```
  
</details>

##  معادلة خالد 
**الفكرة:** تجربة جميع الاحتمالات


<details>
  <summary>الحل بلغة C++</summary>

```c++
#include <iostream>
using namespace std;

const int P = 35171; // معطيات المسألة
const int A = 24636; // معطيات المسألة

int main()
{
    for (long long x = 1; x <= 1000000; x++)
    {
        if (x * A % P == 1)
        {
            cout << x;
            break;
        }
    }
}
```
  
</details>

<details>
  <summary>الحل بلغة بايثون</summary>

```py
P = 35171
A = 24636

for x in range(1, 1000000):
    if (x * A % P == 1):
        print(x)
        exit()
```
  
</details>

##  الاستدعاء الذاتي لعبير 

<details>
 <summary>خوارزمية الاستدعاء الذاتي (ريكيرجن / Recursion)</summary>
 <b>الفكرة:</b> تطبيق العطيات بتحويل المسألة إلى دالة ثم استدعائها كل مرة، وتذكر النتائج السابقة (memoization)

  
 <details>
   <summary>الحل بلغة C++</summary>

```c++
#include <iostream>
using namespace std;

const int N = 257; // اكتب الرقم المطلوب
const int MOD = 193; // اكتب الرقم بعد باقي القسمة

int memo[N+1];
int rec(int i)
{
    if (memo[i] != -1)
        return memo[i];
    return memo[i] = (rec(i-3) + rec(i-2) * rec(i-1)) % MOD;
}

int main()
{
    memset(memo, -1, sizeof memo);
    memo[1] = 1;
    memo[2] = 2;
    memo[3] = 3;
    cout << rec(N);
}
```
  
 </details>

 <details>
  <summary>الحل بلغة بايثون</summary>

```py
N = 257 # اكتب الرقم المطلوب
MOD = 193 # اكتب الرقم بعد باقي القسمة

memo = [-1] * N+1;
def rec(i: int) -> int:
    if (memo[i] != -1):
        return memo[i]
    return memo[i] = (rec(i-3) + rec(i-2) * rec(i-1)) % MOD;

memo[1] = 1
memo[2] = 2
memo[3] = 3
print(rec(N))
```

 </details>

</details>


<details>
  <summary>الحل باستخدام البرمجة الديناميكية (Dynamic Programming / DP)</summary>
  <b>الفكرة: تطبيق المعادلة كما هي</b>

 <details>
  <summary>الحل بلغة C++</summary>

```c++
#include <iostream>
using namespace std;

const int N = 257; // اكتب الرقم المطلوب
const int MOD = 193; // اكتب الرقم بعد باقي القسمة

int dp[N+1];

int main()
{
    dp[1] = 1;
    dp[2] = 2;
    dp[3] = 3;
    for (int i = 4; i <= N; i++)
        dp[i] = (dp[i-3] + dp[i-2] * dp[i-1]) % MOD;
    cout << dp[N];
}
```

 </details>

<details>
  <summary>الحل بلغة بايثون</summary>

```py
N = 257 # اكتب الرقم المطلوب
MOD = 193 # اكتب الرقم بعد باقي القسمة

dp = [0] * N+1
dp[1] = 1
dp[2] = 2
dp[3] = 3
for i in range(4, N+1):
    dp[i] = (dp[i-3] + dp[i-2] * dp[i-1]) % MOD;
print(dp[N])
```

</details>

</details>

##  واجب ريم المنزلي


<details>
  <summary>البحث الثنائي (Binary Search)</summary>

**الفكرة:** وجود حد أعلى للإجابة (نسميه $أ$) وحد أعلى للإجابة (نسميه $ب$)، ثم نختار عدد في المنتصف $\frac{ب + أ}{2}$، ونغير الحد الأدنى والأعلى بناءً على نتيجة الدالة لهذا الرقم.

**ملاحظة:** يمكن تطبيق هذه الفكرة يدويًا باستعمال الحاسبة أو برامج الرسم البياني دون الحاجة لكتابة برنامج
<details>
  <summary>الحل بلغة C++</summary>

```c++
#include <bits/stdc++.h>
using namespace std;

const long double Y = 482.15385787945286;
const long double PREC = 1e-4;

#define f(x) (x+exp(x/100))

int main()
{
    long double l = 1, r = 10000;
    while (abs(l - r) > PREC)
    {
        long double mid = (l + r) / 2;
        if (f(mid) <= Y)
            l = mid;
        else
            r = mid - PREC;
    }
    cout << fixed << setprecision(4) << l;
}
```

  </details>

  <details>
   <summary>الحل بلغة بايثون</summary>

```py
from math import *

Y = 482.15385787945286;
PREC = 1e-4;

def f(x):
    return (x+exp(x/100))

l = 1, r = 10000
while (abs(l - r) > PREC):
    mid = (l + r) / 2;
    if (f(mid) <= Y):
        l = mid;
    else:
        r = mid - PREC;
    
print(l)
```

  </details>
</details>

##  الأعداد الجيدة 

**الفكرة:** تجربة جميع الاحتمالات

<details>
  <summary>الحل بلغة C++</summary>

```c++
#include <bits/stdc++.h>
using namespace std;

const int L = 207418; // نضع هنا قيم المعطيات 
const int R = 691140; // نضع هنا قيم المعطيات 

bool isgood(int xx)
{
    string x = to_string(xx);
    int a=x[0]-'0';
    int b=x[1]-'0';
    int c=x[2]-'0';
    int d=x[3]-'0';
    int e=x[4]-'0';
    int f=x[5]-'0';
    return (a*c+d*f) == (a+b)*e-f;
}

int main()
{
    int sol = 0;
    for (int i = L; i <= R; i++)
        sol += isgood(i);
    cout << sol;
}
```
  
</details>

<details>
  <summary>الحل بلغة بايثون</summary>

```py
L = 207418 # نضع هنا قيم المعطيات 
R = 691140 # نضع هنا قيم المعطيات 

def isgood(xx: int) -> int
    x = str(xx);
    a=int(x[0])
    b=int(x[1])
    c=int(x[2])
    d=int(x[3])
    e=int(x[4])
    f=int(x[5])
    return ((a*c+d*f) == (a+b)*e-f ? 1 : 0)

sol = 0;
for i in range(L, R+1):
    sol += isgood(i)
print(sol)
```

</details>




##  المجموعة الجزئية 


<details>
  <summary>تجربة كل الاحتمالات مع خوارزمية الالتقاء في المنتصف (Meet in the middle)</summary>

**الفكرة:** بما أن عدد الاحتمالات عالي جدًا ($= 2^{40} = 10^{12}$ 1 ترليون)، واللغات في المتوسط تنجز ($= 10^8$ 100 مليون) عملية في الثانية، يعني أن البرنامج لو جرب كل الاحتمالات سيستغرق حوالي ساعتين ونصف!

**الاختصار:** نقسم مجموعة الأعداد إلى نصفين، ونجرب جميع الاحتمالات في كل نصف، ثم نجرب كل احتمالات الدمج ونستعمل البحث الثنائي للاختصار الإضافي

  <details>
  <summary>باستعمال الاستدعاء الذاتي (Recursion)</summary>

  <details>
  <summary>الحل بلغة C++</summary>

```c++
#include <bits/stdc++.h>
#define ll long long

using namespace std;

const int a[] = {1697976, 1970865, 1481237, 1583430, 
1537387, 1270113, 1184765, 1668778, 1857442, 1658671, 
1349846, 1399258, 1636211, 1887763, 1659794, 1277974, 
1438563, 1645195, 1161182, 1991079, 1295942, 1848458, 
1932683, 1759741, 1394766, 1267867, 1664286, 1176904, 
1125246, 1210594, 1950651, 1638457, 1927068, 1619366, 
1299311, 1490221, 1090433, 1678885, 1753003, 1347600};
const int C = 46342470;

vector<ll> sum, sum2;
const int n=40;

void rec(int idx, ll sum, int lim, vector<ll> &su)
{
    if (idx == lim) {
        su.push_back(sum);
        return;
    }
    rec(idx+1, sum+a[idx], lim, su);
    rec(idx+1, sum, lim, su);
}

int main()
{
    rec(0, 0, n/2, sum);
    rec(n/2, 0, n, sum2);
    
    sort(sum2.begin(), sum2.end());
    
    ll sol = 0;
    for (ll v1 : sum) {
        ll xx = *(upper_bound(sum2.begin(), sum2.end(), C-v1)-1);
        sol = max(sol, v1+xx);
    }
    cout << sol;
}
```

  </details>


  <details>
  <summary>الحل بلغة بايثون</summary>

```py
import bisect

a = [1697976, 1970865, 1481237, 1583430,
     1537387, 1270113, 1184765, 1668778, 1857442, 1658671,
     1349846, 1399258, 1636211, 1887763, 1659794, 1277974,
     1438563, 1645195, 1161182, 1991079, 1295942, 1848458,
     1932683, 1759741, 1394766, 1267867, 1664286, 1176904,
     1125246, 1210594, 1950651, 1638457, 1927068, 1619366,
     1299311, 1490221, 1090433, 1678885, 1753003, 1347600]
C = 46342470

sum = []
sum2 = []
n = 40

def rec(idx, total, lim, su):
    if idx == lim:
        su.append(total)
        return
    rec(idx + 1, total + a[idx], lim, su)
    rec(idx + 1, total, lim, su)

rec(0, 0, n // 2, sum)
rec(n // 2, 0, n, sum2)

sum2.sort()

sol = 0
for v1 in sum:
    xx = sum2[bisect.bisect_right(sum2, C - v1) - 1]
    sol = max(sol, v1 + xx)

print(sol)
```

  </details>
  

  </details>


  <details>
  <summary>باستعمال تمثيل الأرقام الثنائية (Bitmasks)</summary>

   <details>
   <summary>الحل بلغة C++</summary>

```c++
#include <bits/stdc++.h>
#define ll long long

using namespace std;

const int a[] = {1697976, 1970865, 1481237, 1583430, 
1537387, 1270113, 1184765, 1668778, 1857442, 1658671, 
1349846, 1399258, 1636211, 1887763, 1659794, 1277974, 
1438563, 1645195, 1161182, 1991079, 1295942, 1848458, 
1932683, 1759741, 1394766, 1267867, 1664286, 1176904, 
1125246, 1210594, 1950651, 1638457, 1927068, 1619366, 
1299311, 1490221, 1090433, 1678885, 1753003, 1347600};
const int C = 46342470;

vector<ll> sum, sum2;
const int n=40;

int main()
{   
    const int half = n / 2;
    for (int i = 0; i < (1 << half); i++)
    {
        ll s = 0;
        for (int j = 0; j < half; j++)
        {
            if (i & (1 << j))
                s += a[j];
        }
        sum.push_back(s);
    }
    
    for (int i = 1; i < (1 << half); i++)
    {
        ll s = 0;
        for (int j = half; j < n; j++)
        {
            if (i & (1 << (j - half)))
                s += a[j];
        }
        sum2.push_back(s);
    }
    
    sort(sum2.begin(), sum2.end());
    
    ll sol = 0;
    for (ll v1 : sum) {
        ll xx = *(upper_bound(sum2.begin(), sum2.end(), x-v1)-1);
        sol = max(sol, v1+xx);
    }
    cout << sol;
}
```

   </details>


   <details>
   <summary>الحل بلغة بايثون</summary>

```py
import bisect

a = [1697976, 1970865, 1481237, 1583430,
     1537387, 1270113, 1184765, 1668778, 1857442, 1658671,
     1349846, 1399258, 1636211, 1887763, 1659794, 1277974,
     1438563, 1645195, 1161182, 1991079, 1295942, 1848458,
     1932683, 1759741, 1394766, 1267867, 1664286, 1176904,
     1125246, 1210594, 1950651, 1638457, 1927068, 1619366,
     1299311, 1490221, 1090433, 1678885, 1753003, 1347600]
C = 46342470

sum = []
sum2 = []
n = 40

half = n // 2
for i in range(1 << half):
    s = 0
    for j in range(half):
        if i & (1 << j):
            s += a[j]
    sum.append(s)

for i in range(1, 1 << half):
    s = 0
    for j in range(half, n):
        if i & (1 << (j - half)):
            s += a[j]
    sum2.append(s)

sum2.sort()

sol = 0
for v1 in sum:
    xx = sum2[bisect.bisect_right(sum2, C - v1) - 1]
    sol = max(sol, v1 + xx)

print(sol)
```

   </details>

  </details>

</details>

<details>
  <summary>الحل باستعمال البرمجة الديناميكية (Dynamic Programming / DP)</summary>


  <details>
  <summary>الحل بلغة C++</summary>

```c++
#include <bits/stdc++.h>
using namespace std;

int a[] = {1697976, 1970865, 1481237, 1583430, 
1537387, 1270113, 1184765, 1668778, 1857442, 1658671, 
1349846, 1399258, 1636211, 1887763, 1659794, 1277974, 
1438563, 1645195, 1161182, 1991079, 1295942, 1848458, 
1932683, 1759741, 1394766, 1267867, 1664286, 1176904, 
1125246, 1210594, 1950651, 1638457, 1927068, 1619366, 
1299311, 1490221, 1090433, 1678885, 1753003, 1347600};
const int C = 46342470;

const int N = 5e7; // أكبر قيمة ممكنة
int dp[N];

int main()
{
    dp[0] = 1;
    for (int i = 1; i <= 40; i++) {
        for (int j = N - 1; j > 0; j--) {
            if (j >= a[i]) {
                dp[j] |= dp[j - a[i]];
            }
        }
    }
    int result = 0;
    for (int i = 1; i <= C; i++)
    {
        if (dp[i])
            result = i;
    }
    cout << result;
}
```
        
  </details>


  <details>
  <summary>الحل بلغة بايثون</summary>

```py
a = [1697976, 1970865, 1481237, 1583430,
     1537387, 1270113, 1184765, 1668778, 1857442, 1658671,
     1349846, 1399258, 1636211, 1887763, 1659794, 1277974,
     1438563, 1645195, 1161182, 1991079, 1295942, 1848458,
     1932683, 1759741, 1394766, 1267867, 1664286, 1176904,
     1125246, 1210594, 1950651, 1638457, 1927068, 1619366,
     1299311, 1490221, 1090433, 1678885, 1753003, 1347600]
C = 46342470

N = int(5e7)
dp = [0] * N
dp[0] = 1

for i in range(1, 41):
    for j in range(N - 1, 0, -1):
        if j >= a[i]:
            dp[j] |= dp[j - a[i]]

result = 0
for i in range(1, C + 1):
    if dp[i]:
        result = i

print(result)
```

  </details>

</details>
  
<details>
   <summary>تجربة احتمالات عشوائية</summary>

   <b>ملاحظة: هذه الفكرة قد تطبع أرقام خاطئة، لأنها تعتمد على العشوائية، لكن كل ما زادت عدد المحاولات زادت الدقة، وهي غالبًا تطبع نتائج صحيحة</b>
  
  <details>
  <summary>الحل بلغة C++</summary>


```c++
#include <bits/stdc++.h>
using namespace std;

int a[] = {1697976, 1970865, 1481237, 1583430, 
1537387, 1270113, 1184765, 1668778, 1857442, 1658671, 
1349846, 1399258, 1636211, 1887763, 1659794, 1277974, 
1438563, 1645195, 1161182, 1991079, 1295942, 1848458, 
1932683, 1759741, 1394766, 1267867, 1664286, 1176904, 
1125246, 1210594, 1950651, 1638457, 1927068, 1619366, 
1299311, 1490221, 1090433, 1678885, 1753003, 1347600};
const int C = 46342470;
const int TRIES = 1e5; // عدد المحاولات، 100 ألف محاولة

int main()
{
    int result = 0;
    for (int i=0; i <= TRIES; i++)
    {
        random_shuffle(a, a+n);
        int cur=0;
        for (auto c : v)
        {
            if (cur+c > C)
            {
                result = max(cur,result);
                break;
            }
            cur += c;
        }
    }
    cout << result;
}
```
        

  </details>

  <details>
  <summary>الحل بلغة بايثون</summary>


```py
import random

a = [1697976, 1970865, 1481237, 1583430,
     1537387, 1270113, 1184765, 1668778, 1857442, 1658671,
     1349846, 1399258, 1636211, 1887763, 1659794, 1277974,
     1438563, 1645195, 1161182, 1991079, 1295942, 1848458,
     1932683, 1759741, 1394766, 1267867, 1664286, 1176904,
     1125246, 1210594, 1950651, 1638457, 1927068, 1619366,
     1299311, 1490221, 1090433, 1678885, 1753003, 1347600]
C = 46342470
TRIES = int(1e5)

result = 0
for i in range(TRIES + 1):
    random.shuffle(a)
    cur = 0
    for c in a:
        if cur + c > C:
            result = max(cur, result)
            break
        cur += c

print(result)
```
        

  </details>

</details>

</div>
