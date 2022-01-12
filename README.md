# Ninjas-AnujBhaiya-Insertion-Sort
#include <iostream>

using namespace std;
void InputArray (int arr[],int n){
    for(int i=0;i<n;i++){
        cin>>arr[i];
    }
}
void InsertionSort(int arr[],int n){
    for(int i=1;i<n;i++){
        int temp= arr[i];
        int j=i-1;
        while(j>=0 && arr[j]>temp){
            arr[j+1]=arr[j];
            j--;
        }
        arr[j+1]=temp;
    }
}
void OutputArray (int arr[],int n){
    for(int i=0;i<n;i++){
        cout<<arr[i]<<" ";
    }
}

int main()
{   int n;
    cin>>n;
    int arr[10000];
    InputArray(arr,n);
    InsertionSort(arr,n);
    OutputArray(arr,n);

    return 0;
}
