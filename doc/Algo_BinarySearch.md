---
title: Algorithm-BinarySearch
layout: default
---

{% highlight cpp %}
void binarysearch(int data[], int search, int length){
    int low = 0;
    int high = length-1;
    while (low <= high){
        int mid = (low + high) / 2;
        if (data[mid] == search){
            printf("\nIndex:%d", mid);
            return 0;
        }
        else if (data[mid] > search){
            high = mid - 1;
        }
        else if (data[mid] < search){
            low = mid + 1;
        }
    }
    printf("Not found");
}
{% endhighlight %}