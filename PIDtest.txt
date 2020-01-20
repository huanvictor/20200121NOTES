#include<stdio.h>
#include<string.h>

typedef struct PID{
double setpoint;
double Propertion;
double Integral;
double derivative;
double lasterror;
double preerror;
double sumerror;
}PID;

/*PID 计算部分函数*/
double PIDcal(PID*pp,double Nextpoint)
{
double dError,Error;
Error=pp->setpoint-Nextpoint;
pp->SumError+=Error;
dError=pp->Lasterror-pp->preError;

pp->preerror=pp->lasterror;
pp->lasterror=error;
return(pp->propertion*error
+pp->integral*pp->*sumerror
+pp->derivative*dError)
}

/*初始化PID*/
void PIDInit(PID*pp)
{}

/*传感器*/
double sensor（void）
{
	return 100.0；
}
void main(void)
{
	PID sPID;
	double rout;
	double rin;
	PIDInit(&sPID)
	
	sPID.Proportion=0.5;
	sPID.Integral=0.5;
	sPID.Derivative=0.0;
	sPID.setpoint=100.0;
	for(; ;)
{
	rin=sensor();
	rout=PIDcal(&sPID,rin);
	actuator(rout);


}
