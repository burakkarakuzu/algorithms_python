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
  <h1><ins>Selected Sort</ins></h1>
  <pre>
  <code>
  def selectSort(A):
    for i in range(len(A)):
        min=i
        for j in range(i+1,len(A)):
            if A[min]>A[j]:
                min=j
        A[i],A[min]=A[min],A[i]
  </pre>
  </code>
  <br><br>
  <h1><ins>Bubble Sort</ins></h1>
  <img src="https://user-images.githubusercontent.com/95481169/167299276-b549477d-cf91-4856-b308-64d5601d841d.png"/>
  <pre>
  <code>
  def bubbleSort(arr):
    n=len(arr):
    for i in range(n):
        swapped=False
        for j in range(0,n-i-1):
            if arr[j]>arr[j+1]:
                arr[j],arr[j+1]=arr[j+1],arr[j]
                swapped=True
        if swapped==False:
            break

  </code>
  </pre>
  
</body>
</HTML>
