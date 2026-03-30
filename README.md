
# EXPT.NO-7-IMPLEMENTATION-OF-GO-BACK-N-PROTOCOL-SLIDING-WINDOW
# AIM
To write and execute a program for Go-Back-N protocol.
# EQUIPMENTS REQUIRED
Personal Computer Turbo C Compiler
# PROCEDURE
1.	Connect two computers in Wired/Wireless LAN.
2.	Make sure that two computers are in one network and could able to ping each other.
3.	In the codeblocker open new c file and type the program.
4.	In the menu choose->Project->Properties->Project Build options->Linker settings->Add netproto and pthread.
5.	Execute the program in both server and client.
6.	Enter the IP address of the remote machine, port address of both local & remote machine and error rate.
7.	Choose the file and verify the go back protocol operation.

# PROGRAM
```C
#include<stdio.h>
void main()
{

int i,j,n;
printf("GO BACK N ARQ\n");
//printf("Entermessage in format\n");
printf("Enter number of frame : ");
scanf("%d",&n);
char frame[n][10];

for(i=1;i<=n;i++)
{
printf("Content for frame %d :",i);
scanf("%s",&frame[i]);
}
int s=1;
//while(j<=n){
printf("Enter frame number with no ACK :");
scanf("%d",&j);
for(i=1;i<=n;i++)
{
if(i!=j)
printf("\n Sending frame %d \n FRAME ACKNOWLEDGED. .... \n",i);
//else
//printf("\n Frame not Acknowledeged. ....... \n");
}
if(j<=n)
{
printf("No Acknowlegement for frame %d... \n",j);
printf("Resending... Content from frame %d :%s\n\n",j,frame[j]);

}
printf("\n Sending frame %d \n FRAME ACKNOWLEDGED. .... \n",j);
//}

printf("\n\nALL FRAME RECIEVED SUCCESSFULLY\n\n");
}
```
# OUTPUT

<img width="1021" height="845" alt="image" src="https://github.com/user-attachments/assets/aa471b4d-4850-49b8-9fdc-cc449b3d1c83" />

# RESULT 

Thus the Go-Back-N protocol-Sliding Window was implemented and the output is verified successfully.
