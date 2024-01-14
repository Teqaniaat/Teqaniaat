---
title: 'ATHKA Roadmap'
layout: athkaAR
lang: ar
---
# خطة الاستعداد والتدريب لأولمبياد أذكى
### برامج ينصح بها لكتابة وتنفيذ النصوص البرمجية
- ـCodeBlocks | قديم & خفيف & ++C فقط
- ـVisual Studio Code | قابل للتخصيص & خفيف & جميع اللغات
- ـVisual Studio | متقدم & ثقيل & جميع اللغات
- ـPycharm community | خفيف & python فقط

أو بإمكانك استخدام سطر الأوامر (cmd line).

## تعلم أساسيات البرمجة
انت بحاجة الى تعلم أساسيات البرمجة فقط، مسائل الأولمبياد لا يتطلب معرفة المشارك لمفاهيم متقدمة بالبرمجة مثل "البرمجة الكائنية"
اساسيات البرمجة المطلوبة: 
- الإدخال / الإخراج
- التكرار
- الأوامر الشرطية
- الدوال 
- أنواع المتغيرات الأساسية والعمليات عليها
- العمليات الثنائية -Bitwise operations-
- السلاسل النصية والعمليات عليها
- نوع المتغير struct ( اختياري ) 
- المؤشرات -pointers- ( اختياري )

**مصدر عربي لتعلم أساسيات برمجة لغة سي بلس بلس:** [Harmash](https://harmash.com/tutorials/cplusplus/overview)
**مصدر عربي لتعلم أساسيات برمجة بلغة بايثون:** [Harmash](https://harmash.com/tutorials/python/overview)

**مصدر انقليزي لتعلم أساسيات برمجة لغة سي بلس بلس:** [W3Schools](https://www.w3schools.com/cpp/)
**مصدر انقليزي لتعلم أساسيات برمجة لغة بايثون:** [W3Schools](https://www.w3schools.com/python/)


في حال واجهتك أي مشكلة اثناء التعلم، يوتيوب وقوقل ما بيقصرون معك، بإمكانك أيضا البحث في المجتمعات.


**الوقت المتوقع لتعلم أساسيات البرمجة:>أسبوعين**

## الخوارزميات
### ( عند البحث عن خوارزمية/مفاهيم/تقنيات بشكل عام ينصح بالاعتماد على تسميتها الإنقليزية لنتائج أفضل )
هنا أهم الخوارزميات المستهدفة في الأولمبياد:
- تعقيد الخوارزميات -Time Complexity-
- خوارزميات الرياضيات/الاستراتيجيات الحسابية
  - التحقق الأعداد الأولية -Prime Test-
  - القواسم -Divisors-
  - تحليل الأعداد الأولية -Prime Factorization-
  - حدسية جولدباخ -Goldbach Conjecture-
  - خوارزمية ايجاد الأعداد الأولية -sieve of eratosthenes-
  - القاسم المشترك الأكبر/المضاعف المشترك الأصغر -GCD/LCM-
  - الأسس الثنائية -Binary Exponentiation-
  - المصفوفات -Matrices-
- تقنيات وخوارزميات عامة
  - خوارزمية البحث الثنائي -Binary Search-
  - البحث بين نقطتين -Two Pointers-
  - مجموع البادئة -Prefix sum-
  - استراتيجية فَرِّق تَسُدْ -Divide and conquer-
- الهندسة -Geometry-
  - نظرية فيثاغورس -Pythagorean theorem-
  - المتجهات -Vectors-
  - تقاطع الخطوط -Line intersection-
  - اختبار موقع النقطة -Point Location Test-
  - استراتيجية -Sweep Line-
- خوارزميات الرسوم البيانية -Graph Algorithms-
  - البحث بالعمق -DFS-
  - البحث بالعرض -BFS-
  - خوارزمية -Dijkstra-
  - خوارزمية -MST-
  - الترتيب الطوبولوجي -Topological Sort-
- الخوارزميات الارتدادية/العودية -backtracking-
  - الدوال ذاتية الاستدعاء -recursion- 
- البرمجة الديناميكية -Dynamic Programming-
  - العد التوافيقي -Combinatorical Counting-
  - البرمجة الديناميكية على الاعداد الثنائية -Bitmask DP-
  - التحسين -Optimization problems-
  - البرمجة الديناميكية على الرسوم البيانية -DP on trees-
- هياكل البيانات
  - الطابور -Queue-
  - المكدس -Stack-
  - المجموعة المنفصلة -Disjoint-set data-
  - الشجرة المجزئة -Segment Tree-
  - تحليل الجذور -Sqrt decomposition-
  - الجد الأدنى المشترك -Lowest Common Anceastor-
- اهم دوال ++C المدمجة
  - ـ `sort`
  - ـ `lower_bound`/`upper_bound`/`binary_search`
  - ـ `min`/`max`
  - ـ `min_element`/`max_element`
  - ـ `swap`
  - ـ `reverse`
  - ـ `builtin_popcount`
  - ـ `memset`
  - ـ `gcd`/`lcm`
- ـ اهم هياكل البيانات المدمجة في ++C
  - ـ `vector`
  - ـ `set`/`multiset`/`unordered_set`
  - ـ `map`
  - ـ `pair`
  - ـ `stack`
  - ـ `queue`
  - ـ `priority_queue`
  - ـ `array`

### مصادر تعلم الخوارزميات بالعربية
- [برمجة تنافسية بالعربية](https://www.youtube.com/@ArabicCompetitiveProgramming) 
<!-- - مدونة البرمجة التنافسية العربية -->

### مصادر تعلم الخوارزميات بالإنقليزية
- [كتيب البرمجة التنافسية (CPH)](https://cses.fi/book/book.pdf)
- [IUSACO Cpp](https://darrenyao.com/usacobook/cpp.pdf)
- [دليل USACO](https://usaco.guide/)
- [خوارزميات CP](https://cp-algorithms.com/)
- [GeeksForGeeks](https://www.geeksforgeeks.org/competitive-programming-a-complete-guide/)
- [قناة Errichito](https://www.youtube.com/c/Errichto)


## للتدريب على طريقة اسئلة الأولمبياد -البرمجة التنافسية | Competative Programming-
- [مجموعة مسائل جامعة أسيوط](https://codeforces.com/group/MWSDmqGsZm/contests)
- [مجموعة مسائل Errichto](https://codeforces.com/group/yg7WhsFsAp/contests)

**الوقت المتوقع للتدريب: إلى الأبد**

## ملاحظات
- بعض المسائل تحتاج إلى معرفة خوارزمية معينة حتى تحلها، بإمكانك تعلم الخوارزمية أو تجاهل المسألة حتى تصل إلى ذلك المستوى.
- البرمجة الديناميكية تعتمد إلى حد كبير على عدد مسائل البرمجة الديناميكية المختلفة التي تم حلها.
