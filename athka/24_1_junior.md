---
title: 'حلول الاختبار التأهيلي (المرحلة المتوسطة)'
description: 'أذكى 2024 باللغتين: C++ وبايثون'
lang: ar
layout: redirect
redirect: "/athka/24_1_junior"
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

{% include /athka/if-condition.md %}

## التكرار

{% include /athka/for-loop.md %}

## المجموع الضخم 
**المسألة:** لديك في المعطيات متغيرين اثنين، المطلوب جمع جميع الارقام التي تقع بينهم مع تضمين المتغيرين في الحساب 

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
**ملخص المسألة:** تعطى عددين صحيحين $P$ و $A$، أوجد الرقم $X$ الذي يحقق هذه المعادلة:
$$X \cdot A mod P = 1$$

حيث أن عملية $mod$ تعني باقي القسمة

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
**ملخص المسألة:** تعطى رقمين، أوجد باقي القسمة (مثلًا $\frac{15}{4} = 3$ والباقي الذي لا يقبل القسمة يكون $3$)
<details>
  <summary>استخدام عملية باقي القسمة مباشرة (بلغة بايثون فقط)</summary>

```python
N = 20350185920713548059742215227885673608992288193593
print(N%389)
```

</details>
 
<details>
  <summary>استخدام عملية باقي القسمة بتسلسل محدد (بلغة C++)</summary>

```c++
#include <iostream>
using namespace std;
const string N = "20350185920713548059742215227885673608992288193593";
const int M = 389;
int main()
{
    int result = 0;
    for(int i=0; i<N.size(); i++)
        result = (result*10 + N[i]-'0') % M;
    cout << result;
}
```
        
</details>


##  المجموعة الجزئية 

{% include /athka/subset-easy.md %}
