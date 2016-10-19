# BurstTime2

/**

  First Come First Served Algorithm 
  Author: Davide Spano

*/
#include <iostream> 

int main()
{
	int processCount; //mi dice quanti processi voglio inserire nel mio algoritmo
	std::cout<<"Insert the number of processes:"<<std::endl;
	std::cin >> processCount;
	
	int burstTime[processCount];
	int waitingTime[processCount];
	int tournaroundTime[processCount];
	
		for(int i=0;i< processCount; i++)
		{
			std::cout<<"Insert the burst time of the P["<< (i+1) <<"]"<<std::endl;
			std::cin >> burstTime[i]; //passiamo l'indice i
		}
	
		waitingTime[0]=0;
		for(int i =1;i< processCount; i++)
		{
			waitingTime[i]=waitingTime[i-1]+burstTime[i-1]; 
		}
	
	
		
	}
	
	
	return 0;
}

//Excel Table:
// First Come First Served Algorithm 
//   Burst Time |  Waiting Time |  Tournaround Time 
//P1    20              0                 20
//P2    2              20                 22
//P3    2              22                 24
//   (input)         (output)           (output)
