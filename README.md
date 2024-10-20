# Exp-20-Sorting
# Aim
Write a c++ program:
1. To do selection sorting.
2. To do insertion sorting.
3. To do bubble sorting.
# Software Used
VS Code and c++ online compiler.
# Theory
Sorting is the process of arranging the elements of a data structure in a specific order, typically in ascending or descending order.

The Types of Sorting Algorithms:

Bubble Sort: A simple algorithm that repeatedly steps through the list, compares adjacent elements, and swaps them if they are in the wrong order.

Selection Sort: Finds the minimum (or maximum) element from the unsorted part and moves it to the sorted part.

Insertion Sort: Builds the sorted list one element at a time by repeatedly taking an element from the unsorted part and inserting it into the correct position in the sorted part.

# Program Code
```
//Selection Sorting

#include <iostream>
using namespace std;

void swap(int *a, int *b){
    int temp;
    temp = *a;
    *a=*b;
    *b=temp;

}
void s_sort(int *a, int elements){
    int n=0;
    int *b;

    while (n!= elements){
        b = a+1; 
        for(int i = 0; i<(elements-1)-n; i++){
            if(*a > *b) {
                swap(a,b);
            }
            b++;
        }
        n++;
        a++;
    }
}
int main(){
    int no_el;
    cout << "How many elements in your array ? "<<endl;
    cin>>no_el;
    int arr[no_el];
    cout<<"Enter "<<no_el<<" Elements: "<<endl;
    for(int i=0; i<no_el;i++){
        cin>>arr[i];
    }
    cout<<"Sorted Array: ";
    s_sort(&arr[0],no_el);

    for(int i=0; i<no_el;i++){
        cout<<arr[i]<< " ";

    }
    return 0;
}
```
```
//Insertion Sorting

#include <iostream>
using namespace std;

void insertionsort(int arr[], int n){
    for (int i = 1; i<n ; i++){
        int key = arr [i];
        int j =i-1;

        while (j>= 0 &&  arr[j]>key){
            arr[j+1] = arr[j];
            j--;
        }
        arr[j+1]= key;
    }
}
int main(){
    int arr[]= {7, 19, 3, 23, 8};
    int n = sizeof(arr) / sizeof(arr[0]);
    cout<< "Original array: ";
    for (int i =0; i<n;i++){
        cout<<arr[i]<<" ";
    }
    insertionsort(arr,n);
    cout<< "\nSorted array: ";
    for (int i = 0; i< n ; i++){
        cout << arr[i]<<" ";
    }
    return 0;
    }
```
```
//Bubble Sorting

#include<iostream>
using namespace std;

void swap(int* a,int* b){
int temp;
 temp=*a;
*a=*b;
 *b=temp;
}
int main(){
 int elements;
  cout<<"How many elements in the array? :";
  cin>>elements;
   int array[elements];
 cout<<"Enter elements:";
for(int i=0;i<elements;i++){
 cin>>array[i];
 }
for(int i=0;i<elements;i++){
 cout<<array[i]<<" ";
  }
 int n=0;
while(n!=elements){
 for(int i=0;i<elements-n;i++){
if(array[i]>array[i+1]){
swap(&array[i],&array[i+1]);
 }
}
 n++;
 }
 cout<<"\nSorted array is:"<<endl;
for(int i=0;i<elements;i++){
 cout<<array[i]<<" ";
 }
 return 0;
}
```

# Output
### Selection Sorting
![image](https://github.com/user-attachments/assets/1cd7c425-3f47-49c2-a647-3af1459f580c)
### Insertion Sorting
![image](https://github.com/user-attachments/assets/0b681a22-85d8-4056-9957-8ceb06b3267d)
### Bubble Sorting
![image](https://github.com/user-attachments/assets/38aa73ba-ebde-416c-80c5-ba810734abbc)

# Conclusion
We learnt how to do selection sort, insertion sort and bubble sort in c++.
