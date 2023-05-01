# Arrays

#include<stdio.h>

/*
int main(){
	int arr[5];
	for(int i=0;i<=5;i++){
		printf("Enter the element number  %d ",i+1);
		scanf("%d",&arr[i]);
	}
	for(int i=5;i>=0;i--){
		printf("%d\n",arr[i]);
	}
	return 0;
}


int main(){
	int arr[5]={45,90,90,20,34};
	for(int i=0;i<5;i++){
		if (arr[i]<=35) printf("%d\n",i);
		
	}
}


Q.1 To Calculate the product of all the elemnts in the given array

int main(){
	int arr[5] = {2,4,5,6,7};
	int prod = 1;
	for(int i=0;i<5;i++){
		prod *= arr[i];
		
	}
	printf("%d",prod);
	return 0;
}


Q2. To find the maximum value of array
int main(){
	int n;
	printf("Enter the value of array : ");
	scanf("%d",&n);
	int arr[n];
	for(int i = 0;i<=n;i++){
		scanf("%d",&arr[i]);
	}
	int max = -1;
	for(int i = 0;i<=n;i++){
		if (arr[i]> max){
			max=arr[i];
		} 
	}
	printf("Therefore the maximum value is : %d",max);
	return 0;
}


Q3. Find total number of pairs in the Array whose sum is equal to the given value X

int main(){
	int arr[8] = {1,2,3,4,5,6,7,8};
	int count;
	int totalpairs = 0;
	int x= 12;
	for(int i = 0;i<=7;i++){
		for(int j = i+1;j<=7;j++){
			if(arr[i]+arr[j]==x){
				totalpairs++;
				printf("(%d,%d)\n",arr[i],arr[j]);
			}
		}
	}
	printf("%d",totalpairs);
	return 0;
}



Q4. Find total number of triplet pairs in the Array whose sum is equal to the given value X
int main(){
	int arr[8] = {1,2,3,4,5,6,7,8};
	int count;
	int totalpairs = 0;
	int x= 12;
	for(int i = 0;i<=7;i++){
		for(int j = i+1;j<=7;j++){
			for(int k = j+1;k<=7;k++){
				if(arr[i]+arr[j]+arr[k]==x){
				
					totalpairs++;
					printf("(%d,%d,%d)\n",arr[i],arr[j],arr[k]);
				}	
			}
			
		}
	}
	printf("%d",totalpairs);
	return 0;
}

#include<limits.h>


int main(){
	int arr[8] = {1,2,3,4,5,6,7};
	int max = INT_MIN;
	int smax = INT_MIN;
	for(int i = 0;i<=7;i++){
		if(max<arr[i]){
			smax = max;
			max = arr[i];
		}
		else if(smax<arr[i]){
			smax = arr[i];
		}
	}
	
	printf("Therefore the second maximum value is : %d",smax);
	return 0;
}


Q5. to write the array in reverse order
int main(){
	int arr[5] = {1,2,3,4,5};
	int brr[5];
	for(int i = 0;i<5;i++){
		brr[i] = arr[4-i];
	}
	for(int i = 0;i<5;i++){
		printf("%d ",brr[i]);
	}
	return 0;
}



Q6. To reverse the array without generating any other array

void reverse(int arr[]){
	int i=0;
	int j=4;
	while(i<=j){
		int temp = arr[i];
		arr[i]= arr[j];
		arr[j]= temp;
		i++;
		j--;
	}
	return ;
}

int main(){
	int arr[5] = {1,2,3,4,5};
	reverse(arr);
	for(int i = 0;i<5;i++){
		printf("%d ",arr[i]);
	}
	return 0;
}



Q8. To print the reverse of the array from a particular index
void reverse(int arr[],int a,int b){
	for(int i=a,j=b;i<=j;i++,j--){
		int temp = arr[i];
		arr[i]=arr[j];
		arr[j] = temp;
	}
	return ;
}

int main(){
	int a,b;
	int arr[7] = {1,2,3,4,5,6,7};
	printf("Enter the index you want to reverse in the array : ");
	scanf("%d %d",&a,&b);
	reverse(arr,a,b);
	for(int i = 0;i<=6;i++){
		printf("%d ",arr[i]);
	}
	return 0;
}



Q9. To find reverse a array with a large chunk of value
void reverse(int arr[],int a,int b){
	for(int i=a,j=b;i<=j;i++,j--){
		int temp = arr[i];
		arr[i]=arr[j];
		arr[j] = temp;
	}
	return ;
}

int main(){
	int a,b;
	int arr[7] = {1,2,3,4,5,6,7};
	int n = 7;
	int k = 50;
	k=k%n;
	reverse(arr,0,n-1);
	reverse(arr,0,k-1);
	reverse(arr,k,n-1);
	for(int i = 0;i<=6;i++){
		printf("%d ",arr[i]);
	}
	return 0;
}



Q10. To find a particular index of the number 
int main(){
	int arr[7] = {1,2,3,4,5,6,7};
	int x = 5;
	for(int i = 0;i<=6;i++){
		if(arr[i]==x){
			printf("%d is present in index : %d",x,i);
			break;
		}
	}
	return 0;
}


Q10. To find a multiple index of the number in the array
int main(){
	int arr[7] = {1,2,3,4,5,6,7};
	int x = 5;
	for(int i = 0;i<=6;i++){
		if(arr[i]==x){
			printf("%d is present in index : %d",x,i);
			
		}
	}
	return 0;
}


#include<stdbool.h>
//Q12. To find a particular index of the number[Linear search] 
int main(){
	int arr[7] = {1,2,3,4,5,6,7};
	int x = 5;
	int idx = -1;
	bool flag = false;
	for(int i = 0;i<=6;i++){
		if(arr[i]==x){
			flag = true;
			idx = i;
			break;
			
		}
	}
	if(flag == false){
		printf("%d is not present in the array",x);
	}
	else{
		printf("%d is present in the array and its index is : %d",x,idx);
	}
	return 0;
}


Q13. TO find the duplicate value in the array
 int main(){
	int arr[7] = {1,2,7,4,5,6,7};
	for(int i=0;i<=6;i++){
		for(int j = i+1;j<=6;j++){
			if(arr[i]==arr[j]){
				printf("%d is the duplicate number",arr[i]);
				break;
			}
		}
	}
	return 0;
}
*/


// To find the unique value in the array

#include<stdbool.h>
int main(){
	int arr[7] = {1,2,3,2,1,2,1};
	for(int i=0;i<=6;i++){
		bool flag = false;
		for(int j = i+1;j<=6;j++){
			if(arr[i]==arr[j]){
				flag = true;
			}
		}
		if(flag==false){
			printf("%d",arr[i]);
			break;
		}
	}
	return 0;
}
