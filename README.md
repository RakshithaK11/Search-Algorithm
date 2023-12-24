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
~~~
''' 
Program for linear search method to match the item in a list
Developed by:RAKSHITHA K
RegisterNumber: 23003887
'''
def linearSearch(array,n,k):
    for i in range(0,n):
        if(array[i]==k):
            return i
    return -1
array=eval(input())
k=eval(input())
n=len(array)
array.sort()
result=linearSearch(array,n,k)
if(result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
~~~
ii)	# Find the element in a list using Binary Search(Iterative Method).
~~~
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by:Rakshitha K
RegisterNumber:23003887 
'''
def BinarySearchIter(arr, k, low, high):
    while low<=high:
        mid=low+(high-low)//2
        if arr[mid]==k:
            return mid
        elif arr[mid]<k:
            low=mid+1
        else:
            high=mid-1
    
    return -1
arr=eval(input())
arr.sort()
k=eval(input())
result=BinarySearchIter(arr,k,0,len(arr)-1)
if(result==-1):
    print(arr)
    print("Element not found")
else:
    print(arr)
    print("Element found at index: ",result)
~~~
iii)	# Find the element in a list using Binary Search (recursive Method).
~~~
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: RAKSHITHA K
RegisterNumber:23003887 
'''
def BinarySearch(arr, k, low, high):
    while high>=low:
        mid=low+(high-low)//2
        if arr[mid]==k:
            return mid
        elif arr[mid]>k:
            return BinarySearch(arr, k, low, mid-1)
        else:
            return BinarySearch(arr, k, mid+1, high)
    else:
            return -1
arr=eval(input())
arr.sort()
k=eval(input())
result=BinarySearch(arr,k,0,len(arr)-1)
if(result==-1):
    print(arr)
    print("Element not found")
else:
    print(arr)
    print("Element found at index: ",result)
~~~
## Sample Input and Output
![image](https://github.com/RakshithaK11/Search-Algorithm/assets/139336455/ba579da5-f201-4552-b7d1-09e04ffd6e3d)
![image](https://github.com/RakshithaK11/Search-Algorithm/assets/139336455/d0430525-c8e9-4f52-b9c9-71cf9d128eeb)
![image](https://github.com/RakshithaK11/Search-Algorithm/assets/139336455/351ef4a5-c0c2-430c-b5f5-8aa06ed4e9fd)











## Result
Thus the linear search and binary search algorithm is implemented using python programming.
