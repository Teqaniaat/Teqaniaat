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
