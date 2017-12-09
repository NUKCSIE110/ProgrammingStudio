---
title: ConceptProblems
layout: default
---

## 1.為什麼我的pow()不能用
> **pow:模稜兩可的呼叫多載函式**
pow()函式在C99的定義是  
{% highlight cpp %}
double pow  (double base, double exponent);
float powf (float base, float exponent);
long double powl (long double base, long double exponent);
{% endhighlight %}
所以，使用pow()時引入的參數必須是float,double,long double這三種型態才不會出現多載問題  