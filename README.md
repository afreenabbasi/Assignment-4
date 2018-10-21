#include <stdio.h>
#include <stdlib.h>
#include <pthread.h>

int arr[1000];
	int a=1;
	int c=0;

void * TestThread(void *arg)
{

	int sum = (int)arg;
	for(int i=a; i<100; i++){		
	        sum = sum + arr[i];		
	}
	return ((void*)sum);
}

int main ()
{
	
	int status_t1;
	pthread_t thread_t1;
	for(int i=1;i<=1000;i++){
		arr[i]=i;
		
	}
//creating threads
    int n=0;
	for(int i=0;i<10;i++){
			pthread_create(&thread_t1[i],NULL,TestThread,(void*)(n));
		    n=n+100;
	}
		for(int i=0;i<10;i++){
			pthread_join(thread_t1[i],(void**) & status_t1[i])

		}
		for(int i=0;i<10;i++){
			status[i]=sum+status[i]
		}
	
	printf("\nValue returned By Thread %d\n", status_t1);

	return 0;
}
