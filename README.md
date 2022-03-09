# Codeforces-144A
#include <iostream>
 
using namespace std;
 
int main(){
  int n,arr[105];
  cin >> n;
  for(int i=1;i<=n;i++){
    cin >> arr[i];
  }
  int max = arr[1];
  int min = arr[n];
  int max_index = 1;
  int min_index = n;
  for(int i=1;i<=n;i++){
    if(arr[i] > max){
      max = arr[i];
      max_index = i;
    }
  }
  for(int i=n;i>0;i--){
    if(arr[i] < min){
      min = arr[i];
      min_index = i;
    }
  }
 
  if(max_index < min_index){
    cout << max_index - 1 + n - min_index;
  }
  else{
    cout << max_index + n - min_index - 2;
  }
  
  return 0;
}
