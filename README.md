Can all numbers of an array be made equal in Python
In this article we will see a program to check Can all numbers of an array be made equal in Python. We are given with an array and need to check If it is possible to make all the array elements equal with the given operation then print Yes else print No.

can all elements of array be equal in python
Example
Input : arr[]=[50,75,100]
50 - 50*2*3=300,
75 - 75*2*2=300,
100 - 100*3=300
Hence, Elements of an array can be made equal
Key-Point
A positive integer number can be factorized as prime factors and written as 2a * 3b * 5c * 7d *…
We can multiply given numbers by 2 and 3 so we can increase a and b for them.
So we can make all a and b equal by increasing them to the same big value.
But we can’t change powers of other prime numbers so they must be equal from the beginning.
We can check it by diving all numbers from input by two and by three as many times as possible. Then all of them must be equal.
Algorithm:
Iterate the array and check if the number is divisible by 2
If it is divisible, divide the array element by 2
Similarly, check if the array element is divisible by 3
If it is divisible, divide the array element by 3.
Then, check the remaining elements with the first element of the array.
If they are equal, the array can be made equal.
Code in Python
#Function to check whether an array is equal or not
def check(array,length):
     for i in range(0, length):
     
          # Divide number by 2
            while array[i] % 2 == 0:
                array[i] //= 2

          # Divide number by 3
            while array[i] % 3 == 0:
                array[i] //= 3

     if array[i] != array[0]:
         return False

     return True

#input array from user
array = [50, 100, 75]

#determine length of array and assign to length variable
length=len(array)

if check(array, length):
     print("Yes, all the elements of an array can be made equal")
else:
     print("No, all the elements of an array cannot be made equal")
Output
Yes, all the elements of an array can be made equal
