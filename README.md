# algorithms_python
<HTML>
<body>
  <h1><ins>Binary Search</ins></h1>
<img src="https://user-images.githubusercontent.com/95481169/163147137-7258928a-6ffa-4b0d-8a79-e4c4e254fe31.png" />
<pre>
<code>
def binarySearch(numbers, low, high, x):
    if (high >= low):
        mid = low + (high - low)//2
        if (numbers[mid] == x):
            return mid
        elif (numbers[mid] > x):
            return binarySearch(numbers, low, mid-1, x)
        else:
            return binarySearch(numbers, mid+1, high, x)
    else:
        return -1
numbers = [ 1,4,6,7,12,17,25 ]   #binary search requires sorted numbers
x = 7
result = binarySearch(numbers, 0, len(numbers)-1, x)
if (result != -1):
    print("Search successful, element found at position ", result)
else:
    print("The given element is not present in the array")
</code>
</pre>
<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQX3rVLSpGIVi5TPpn-0xjIen3a68ZbI03IjTUGXL4Th-ucWeDIuCa8zaj5fQ-jgc03tj4&usqp=CAU" />
<img src="quadratic-time.png" />
</body>
</HTML>
