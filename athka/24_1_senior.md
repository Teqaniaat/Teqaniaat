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
    <li>معاذ القرني <a href="https://twitter.com/Muaath_dev">(@Muaath_dev)</a></li>
    <li>يزن آشي <a href="https://twitter.com/ayazashy">(@ayazashy)</a></li>
</ul>

{% include athka-tgchannel.html %}

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

## العبارة الشرطية IF

{% include /athka/if-condition.md %}

## التكرار

{% include /athka/for-loop.md %}

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

{% include /athka/subset-hard.md %}
