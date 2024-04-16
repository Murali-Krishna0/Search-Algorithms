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
i)	#Use a linear search method to match the item in a list.
```
# Developed by : Murali Krishna S
# Register Number : 212223230129

def search(array,key,n):
    for i in range(0,n):
        if key == array[i]:
            return i
    return -1

array = eval(input())
key = int(input())
n = len(array)
array.sort()
print(array)
result = search(array,key,n)
if result == -1:
    print("Element not found")
else:
    print("Element found at index: ",result)



```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
# Developed by : Murali Krishna S
# Register Number : 212223230129

def binary(array,key,high,low):
    while(low<=high):
        mid = low + (high-low)//2
        if array[mid]==key:
            return mid
        elif array[mid]<key:
            low = mid + 1
        elif array[mid]>key:
            high = mid-1
    return -1        
array = eval(input())
key = int(input())
array.sort()
n = len(array)
low,high = 0,len(array)-1
print(array)
result = binary(array,key,high,low)
if result == -1:
    print("Element not found")
else:
    print("Element found at index: ",result)




```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
# Developed by : Murali Krishna S
# Register Number : 212223230129

def binary(array,key,high,low):
    if high>=low:
        mid = low +(high-low)//2
        
        if array[mid]==key:
            return mid
        elif array[mid]<key:
            return binary(array,key,high,mid+1)
        elif array[mid]>key:
            return binary(array,key,mid-1,low)
    return -1        
array = eval(input())
key = int(input())
array.sort()
n = len(array)
low,high = 0,len(array)-1
print(array)
result = binary(array,key,high,low)
if result == -1:
    print("Element not found")
else:
    print("Element found at index: ",result)




```
## Sample Input and Output
![image](https://github.com/Murali-Krishna0/Search-Algorithms/assets/149054535/4ac2220d-457f-48c3-8f0c-0ddf91bec2ec)
![image](https://github.com/Murali-Krishna0/Search-Algorithms/assets/149054535/78b7e5e5-1c3a-4c22-afb7-08706e32cebc)
![image](https://github.com/Murali-Krishna0/Search-Algorithms/assets/149054535/86ecdfca-9710-47df-b0c9-efc2582c21ee)
![image](https://github.com/Murali-Krishna0/Search-Algorithms/assets/149054535/350f5bfc-b710-45a0-b212-686780e29bf9)
![image](https://github.com/Murali-Krishna0/Search-Algorithms/assets/149054535/426e8f68-a2bf-423a-ba56-9c38af383c1d)
![image](https://github.com/Murali-Krishna0/Search-Algorithms/assets/149054535/48325850-4abc-4077-9766-5b362d7e97dc)






## Result
Thus the linear search and binary search algorithm is implemented using python programming.
