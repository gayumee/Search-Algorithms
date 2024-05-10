# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
```
Developed by: T. Gayathri
Reg No: 212223100007
```

i)	#Use a linear search method to match the item in a list.
```
def linear_search(arr, target):
    for i in range(len(arr)):
        if arr[i] == target:
            return i  
    return -1  
arr = eval(input())
target = int(input())
arr.sort()
print(arr)
result = linear_search(arr, target)
if result != -1:
    print("Element found at index: ", result)
else:
    print("Element not found")
```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
def binary_search(arr, target):
    left, right = 0, len(arr) - 1

    while left <= right:
        mid = (left + right) 
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    return -1

arr = eval(input())
target = int(input())
arr.sort()
print(arr)
result = binary_search(sorted(arr), target)

if result != -1:
    print("Element found at index: ", result)
else:
    print("Element not found")
```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
def binary_search_recursive(arr, target, left, right):
    if left <= right:
        mid = (left + right) // 2
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            return binary_search_recursive(arr, target, mid + 1, right)
        else:
            return binary_search_recursive(arr, target, left, mid - 1)
    return -1

arr = eval(input())
target = int(input())
arr.sort()
print(arr)
result = binary_search_recursive(arr, target, 0, len(arr) - 1)
if result != -1:
    print("Element found at index: ", result)
else:
    print("Element not found")
```

## Sample Input and Output
![image](https://github.com/gayumee/Search-Algorithms/assets/149037327/e018c72e-ad03-4b2b-b4ed-b3005279f9a8)
![image](https://github.com/gayumee/Search-Algorithms/assets/149037327/3230afc5-b861-4012-a258-2e848e6afb9a)
![image](https://github.com/gayumee/Search-Algorithms/assets/149037327/514e2bc6-55de-4f23-bf48-83fb23cf879d)


## Result
Thus the linear search and binary search algorithm is implemented using python programming.
