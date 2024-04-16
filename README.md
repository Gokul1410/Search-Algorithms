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

'''
program to search the item in a list using search
Developed by: Gokul C
Register Number: 212223240040
'''

def search(array,key,n):
    for i in range(n):
        if array[i]==key:
            return i
    return -1
array=eval(input())
key=int(input())
n=len(array)
array.sort()
result=search(array,key,n)
print(array)
if (result==-1):
    print("Element not found")
else:
    print("Element found at index: ",result)

```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```

'''
program to search the item in a list using binary search(iterative method)
Developed by: Gokul C
Register Number: 212223240040
'''

def binary(array,key,low,high):
    while(low<=high):
        mid=low+(high-low)//2
        if array[mid]==key:
            return mid
        elif array[mid]<key:
            low=mid+1
        elif array[mid]>key:
            high=mid-1
    return -1


array=eval(input())
key=int(input())
array.sort()
low,high=0,len(array)-1
result=binary(array,key,low,high)
print(array)
if result==-1:
    print("Element not found")
else:
    print("Element found at index: ",result)

```
iii)	# Find the element in a list using Binary Search (recursive Method).
```

'''
program to search the item in a list using binary search(recursive method)
Developed by: Gokul C
Register Number: 212223240040
'''

def binary(array,key,low,high):
    if high>=low:
        mid=low+(high-low)//2
        if array[mid]==key:
            return mid
        elif array[mid]<key:
            return binary(array,key,mid+1,high)
        elif array[mid]>key:
            return binary(array,key,low,mid-1)
    return -1


array=eval(input())
key=int(input())
array.sort()
low,high=0,len(array)-1
result=binary(array,key,low,high)
print(array)
if result==-1:
    print("Element not found")
else:
    print("Element found at index: ",result)

```
## Sample Input and Output

![Screenshot 2024-04-16 171805](https://github.com/Gokul1410/Search-Algorithms/assets/153058321/99809a1d-2434-4843-9812-5783ec1df89c)
![Screenshot 2024-04-16 171817](https://github.com/Gokul1410/Search-Algorithms/assets/153058321/678ece76-fe54-46ce-a1b1-ac066973ad8f)
![Screenshot 2024-04-16 171849](https://github.com/Gokul1410/Search-Algorithms/assets/153058321/adf8d3b0-9755-469c-9d9a-77facec73fd9)
![Screenshot 2024-04-16 171900](https://github.com/Gokul1410/Search-Algorithms/assets/153058321/9bfc5b47-4380-4615-bd72-2afb65479ea5)
![Screenshot 2024-04-16 171913](https://github.com/Gokul1410/Search-Algorithms/assets/153058321/4468164d-1b71-4a39-a3cd-af1d0c4ef4fc)
![Screenshot 2024-04-16 171927](https://github.com/Gokul1410/Search-Algorithms/assets/153058321/607a4295-3201-4b22-b221-8a00f5bcf1c1)


## Result
Thus the linear search and binary search algorithm is implemented using python programming.
