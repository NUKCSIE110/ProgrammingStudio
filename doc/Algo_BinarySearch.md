---
title: Algorithm-BinarySearch
layout: default
---
<script src="https://gist.github.com/kaibaooo/0dd9a6f065445319f88467028baa1a2b.js"></script>


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