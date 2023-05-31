# <p align="center">Single server with infinite capacity (M/M/1):(oo/FIFO)</p>
## Aim :
To find 
* (a) average number of materials in the system 
* (b) average number of materials in the conveyor 
* (c) waiting time of each material in the system 
* (d) waiting time of each material in the conveyor, if the arrival  of materials follow poisson process with the mean interval time 12 seconds, serivice time of lathe machine follows exponential distribution with mean serice time 1 second and average service time of robot is 7 seconds.

## Software required :
Visual components and Python

## Theory:
Queuing are the most frequently encountered problems in everyday life. For example, queue at a cafeteria, library, bank, etc. Common to all of these cases are the arrivals of objects requiring service and the attendant delays when the service mechanism is busy. Waiting lines cannot be eliminated completely, but suitable techniques can be used to reduce the waiting time of an object in the system. A long waiting line may result in loss of customers to an organization. Waiting time can be reduced by providing additional service facilities, but it may result in an increase in the idle time of the service mechanism.

<img width="400" src="https://github.com/ShafeeqAhamedS/PQM_Exp_4_Single-server-infinite-capacity---Markov-Model/assets/93427237/ee6497ea-8cf8-4a2b-b98a-d927cd772dde">

This is a queuing model in which the arrival is Marcovian and departure distribution is also Marcovian,number of server is one and size of the queue is also Marcovian,no.of server is one and size of the queue is infinite and service discipline is 1st come 1st serve(FCFS) and the calling source is also finite.

</br></br>

## Procedure :
<img src="https://github.com/ShafeeqAhamedS/PQM_Exp_4_Single-server-infinite-capacity---Markov-Model/assets/93427237/2f3b6db2-e77b-41a1-ac66-e7f357eb7f0f">

## Experiment:
<img src="https://github.com/Aashima02/Single-server-infinite-capacity---Markov-Model/assets/93427086/cc250870-d1e7-4112-8ccc-5cae2a4301f0">

</br></br></br>

## Program
DEVELOPED BY : Mothesh M
</br>
REG. NO. : 212221230066
```py
arr_time=float(input("Enter the mean inter arrival time of objects from Feeder(in secs):"))
ser_time=float(input("Enter the mean  inter service time of Lathe Machine (in secs) :  "))
Robot_time=float(input("Enter the Additional time taken for the Robot (in secs) :  "))
lam=1/arr_time
mu=1/(ser_time+Robot_time)
print("--------------------------------------------------------------")
print("Single Server with Infinite Capacity - (M/M/1):(oo/FIFO)")
print("--------------------------------------------------------------")
print("The mean arrival rate per second : %0.2f "%lam)
print("The mean service rate per second : %0.2f "%mu)
if (lam <  mu):
    Ls=lam/(mu-lam)
    Lq=Ls-lam/mu
    Ws=Ls/lam
    Wq=Lq/lam
    print("Average number of objects in the system : %0.2f "%Ls)
    print("Average number of objects in the conveyor :  %0.2f "%Lq)
    print("Average waiting time of an object in the system : %0.2f secs"%Ws)
    print("Average waiting time of an object in the conveyor : %0.2f secs"%Wq)
    print("Probability that the system is busy : %0.2f "%(lam/mu) )
    print("Probability that the system is empty : %0.2f "%(1-lam/mu) )
else:
    print("Warning! Objects Over flow will happen in the conveyor")
print("---------------------------------------------------------------")

```

## Output:
![237578218-bc7d4263-d7fe-4d86-9ae3-9cfa63c68b0f](https://github.com/Aashima02/Single-server-infinite-capacity---Markov-Model/assets/93427086/24982b8a-7e5c-46a5-a361-ca5790bd92fa)

## Result:
The average number of material in the sysytem and in the conveyor and waiting time are successfully found.
