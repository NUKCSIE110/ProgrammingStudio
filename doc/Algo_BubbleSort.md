---
title: Algorithm-BubbleSort
layout: default
---
{% highlight cpp %}
void bubble_sort(int nums[], int length){
    for(int i = 0; i < length-1; i++){
        for(int j = 0; j < length-; j++){
            if(nums[j] > nums[j+1]){
                temp = nums[j];
                nums[j] = nums[j+1];
                nums[j+1] = temp;
            }
        }
    }
}
{% endhighlight %}