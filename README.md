# Series Queues with infinite capacity - Open Jackson Network

## AIM :
To find (a) average number of materials in the system (b) average number of materials in the each conveyor of (c) waiting time of each material in the system (d) waiting time of each material in each conveyor, if the arrival  of materials follow Poisson process with the mean interval time 12 seconds, service time of  lathe machine in series follow exponential distribution  with service time  1 second, 1.5 seconds and 1.3 seconds respectively and average service time of robot is 7 seconds.

## SOFTWARE REQUIRED :
Visual components and Python

## THEORY :
![image](https://github.com/harshi1111/Open-Jacson-Networks/assets/84671735/fe192d7e-874a-4cd7-be05-22378b30f231)

## PROCEDURE :
![image](https://github.com/harshi1111/Open-Jacson-Networks/assets/84671735/8058ada6-ff73-497c-8df4-781dd6e6699a)

## EXPERIMENT :
![image](https://github.com/harshi1111/Open-Jacson-Networks/assets/84671735/b69f9fa9-3a68-4998-9a6d-f1f96fdea6b2)

![image](https://github.com/harshi1111/Open-Jacson-Networks/assets/84671735/60d02ed7-f87b-4f75-ba7f-af6ed09ce810)

## PROGRAM :
```
NAME: HARSHITHA V
REG NO: 23002305
```

```
arr_time=float(input("Enter the mean inter arrival time of objects from Feeder (in secs): "))
ser_time1=float(input("Enter the mean  inter service time of Lathe Machine 1 (in secs) :  "))
ser_time2=float(input("Enter the mean  inter service time of Lathe Machine 2 (in secs) :  "))
ser_time3=float(input("Enter the mean  inter service time of Lathe Machine 3 (in secs) :  "))
Robot_time=float(input("Enter the Additional time taken for the Robot (in secs) :  "))
lam=1/arr_time
mu1=1/(ser_time1+Robot_time)
mu2=1/(ser_time2+Robot_time)
mu3=1/(ser_time3+Robot_time)
print("-----------------------------------------------------------------------")
print("Series Queues with infinite capacity- Open Jackson Network")
print("-----------------------------------------------------------------------")
if (lam <  mu1) and (lam <  mu2) and (lam <  mu3):
    Ls1=lam/(mu1-lam)
    Ls2=lam/(mu2-lam)
    Ls3=lam/(mu3-lam)
    Ls=Ls1+Ls2+Ls3
    Lq1=Ls1-lam/mu1
    Lq2=Ls2-lam/mu2
    Lq3=Ls3-lam/mu3
    Wq1=Lq1/lam
    Wq2=Lq2/lam
    Wq3=Lq3/lam
    Ws=Ls/(3*lam)
    print("Average number of objects in the system S1 : %0.2f "%Ls1)
    print("Average number of objects in the system S2 : %0.2f "%Ls2)
    print("Average number of objects in the system S3 : %0.2f "%Ls3)
    print("Average number of objects in the overall system    : %0.2f "%Ls)
    print("Average number of objects in the conveyor S1  :  %0.2f "%Lq1)
    print("Average number of objects in the conveyor S2  :  %0.2f "%Lq2)
    print("Average number of objects in the conveyor S3  :  %0.2f "%Lq3)
    print("Average waiting time of an object in the conveyor S1 : %0.2f secs"%Wq1)
    print("Average waiting time of an object in the conveyor S2 : %0.2f secs"%Wq2)
    print("Average waiting time of an object in the conveyor S3 : %0.2f secs"%Wq3)
else:
    print("Warning! Objects Over flow will happen in the conveyor")
print("----------------------------------------------------------------------")
```

## OUTPUT :
![image](https://github.com/harshi1111/Open-Jacson-Networks/assets/84671735/a0731302-d9d6-4a21-992b-af43e2c02011)

## RESULT :
The average number of material in the sysytem and in the conveyor and waiting time are successfully found.
