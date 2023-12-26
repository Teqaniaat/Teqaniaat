---
title: 'حلول الاختبار التأهيلي (المرحلة المتوسطة)'
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

وهذا الملف ملكية [قناة أذكى](https://t.me/MawhibaNOPAI)


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
            <td>11</td>
            <td>نعم</td>
        </tr>
        <tr>
            <td>التكرار</td>
            <td>17</td>
            <td>نعم</td>
        </tr>
        <tr>
            <td>المجموع الضخم</td>
            <td>20</td>
            <td>نعم</td>
        </tr>
        <tr>
            <td>معادلة خالد</td>
            <td>22</td>
            <td>نعم</td>
        </tr>
        <tr>
            <td>هدية أحمد</td>
            <td>23</td>
            <td>نعم</td>
        </tr>
        <tr>
            <td>المجموعة الجزئية</td>
            <td>24</td>
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


## المجموع الضخم 
**المسألة:**لديك في المعطيات متغيرين اثنين، المطلوب جمع جميع الارقام التي تقع بينهم مع تضمين المتغيرين في الحساب 

<details>
  <summary>استعمال دالة تكرار</summary>

**الفكرة:** انشئ متغير يقوم بالاحتفاظ بالمجموع الكلي وتبدأ بالقيمة 0، بإمكانك عمل دالة تكرار تبدأ من المتغير الاصغر ومن ثم جمعها بالمتغير الذي تم تعريفه مسبقا، وتستمر بالتزايد بمقدار 1 حتى تصل الى قيمة المتغير الاكبر
                
```c++
#include<iostream>
using namespace std;
int main()
{
    int A=1099; // قيمة المتغير الاصغر
    int B=8236; // قيمة المتغير الاكبر
    int counter=0; // المتغير الذي سيقوم بالاحتفاظ بالمجموع الكلي
    for(int i=A; i<=B; i++)
        counter+=i; // زيادة المتغير العداد بمقدار i
    cout<<counter<<endl;
}
```
	
</details>

<details>
  <summary>استعمال معادلة رياضية مباشرة</summary>

**الفكرة:** باستخدام قانون جمع الأعداد من 1 -> n ، الا وهو ( n*(n+1)/2 )، يتم تطبيق القانون على الرقم الاكبر ومن ثم طرح الناتج من ناتج تطبيق القانون على القيمة التي تسبق القيمة الصغرى، حتى نحصل على مجموع الاعداد من A -> B
تصبح المعادلة كالآتي: result = (B*(B+1))/2 - (A*(A-1))/2
                
```c++
#include<iostream>
using namespace std;
int main()
{
    int A=1099; // قيمة المتغير الاصغر
    int B=8236; // قيمة المتغير الاكبر
    int result = (B*(B+1))/2 - (A*(A-1))/2; // المتغير الذي سيقوم بالاحتفاظ بالمجموع الكلي
    cout<<result<<endl;
}
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


## هدية احمد 
<details>
  <summary>بايثون فقط - استخدام عملية باقي القسمة مباشرة</summary>

```python
N = 20350185920713548059742215227885673608992288193593
print(N%389)
```

</details>
 
<details>
  <summary>استخدام عملية باقي القسمة بتسلسل محدد</summary>

```c++
#include <iostream>
using namespace std;
const string N = "20350185920713548059742215227885673608992288193593";
const int M = 389;
int main()
{
    int result=0;
    for(int i=0; i<N.size(); i++)
        result = (result*10 + N[i]-'0') % M;
    cout<<result;
}
```
        
</details>


##  المجموعة الجزئية 


<details>
  <summary>تجربة كل الاحتمالات مع خوارزمية الالتقاء في المنتصف (Meet in the middle)</summary>

**الفكرة:** بما أن عدد الاحتمالات عالي جدًا ($= 2^{32} = 10^{9}$ 1 مليار)، واللغات في المتوسط تنجز ($= 10^8$ 100 مليون) عملية في الثانية، يعني أن البرنامج لو جرب كل الاحتمالات سيستغرق حوالي عشر ثواني!

**الاختصار:** نقسم مجموعة الأعداد إلى نصفين، ونجرب جميع الاحتمالات في كل نصف، ثم نجرب كل احتمالات الدمج ونستعمل البحث الثنائي للاختصار الإضافي

  <details>
  <summary>باستعمال الاستدعاء الذاتي (Recursion)</summary>

  <details>
  <summary>الحل بلغة C++</summary>

```c++
#include <bits/stdc++.h>
#define ll long long

using namespace std;

const int a[] = {570124, 235486, 941944, 489563, 266471, 439987, 433790, 241683, 501957, 551533, 167319, 229289, 669276, 576321, 663079, 285062, 886171, 508154, 700261, 105349, 309850, 378017, 322244, 842792, 365623, 929550, 873777, 879974, 192107, 470972, 948141, 867580};
const int C = 13099613;

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

a = [570124, 235486, 941944, 489563, 266471, 439987, 433790, 241683, 501957, 551533, 167319, 229289, 669276, 576321, 663079, 285062, 886171, 508154, 700261, 105349, 309850, 378017, 322244, 842792, 365623, 929550, 873777, 879974, 192107, 470972, 948141, 867580]
C = 13099613

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

const int a[] = {570124, 235486, 941944, 489563, 266471, 439987, 433790, 241683, 501957, 551533, 167319, 229289, 669276, 576321, 663079, 285062, 886171, 508154, 700261, 105349, 309850, 378017, 322244, 842792, 365623, 929550, 873777, 879974, 192107, 470972, 948141, 867580};
const int C = 13099613;

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

a = [570124, 235486, 941944, 489563, 266471, 439987, 433790, 241683, 501957, 551533, 167319, 229289, 669276, 576321, 663079, 285062, 886171, 508154, 700261, 105349, 309850, 378017, 322244, 842792, 365623, 929550, 873777, 879974, 192107, 470972, 948141, 867580]
C = 13099613

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

int a[] = {570124, 235486, 941944, 489563, 266471, 439987, 433790, 241683, 501957, 551533, 167319, 229289, 669276, 576321, 663079, 285062, 886171, 508154, 700261, 105349, 309850, 378017, 322244, 842792, 365623, 929550, 873777, 879974, 192107, 470972, 948141, 867580};
const int C = 13099613;

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
a = [570124, 235486, 941944, 489563, 266471, 439987, 433790, 241683, 501957, 551533, 167319, 229289, 669276, 576321, 663079, 285062, 886171, 508154, 700261, 105349, 309850, 378017, 322244, 842792, 365623, 929550, 873777, 879974, 192107, 470972, 948141, 867580]
C = 13099613

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

int a[] = {570124, 235486, 941944, 489563, 266471, 439987, 433790, 241683, 501957, 551533, 167319, 229289, 669276, 576321, 663079, 285062, 886171, 508154, 700261, 105349, 309850, 378017, 322244, 842792, 365623, 929550, 873777, 879974, 192107, 470972, 948141, 867580};
const int C = 13099613;
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

a = [570124, 235486, 941944, 489563, 266471, 439987, 433790, 241683, 501957, 551533, 167319, 229289, 669276, 576321, 663079, 285062, 886171, 508154, 700261, 105349, 309850, 378017, 322244, 842792, 365623, 929550, 873777, 879974, 192107, 470972, 948141, 867580]
C = 13099613
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
