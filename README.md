# Q2
import java.util.Scanner;
public class drivers {
 String driver[]={"A","B","C","D","E"};
 String carmodel[]= {"Sedan","HatchBack","Seater","Sedan","HatchBack"};
double rating[]= {3,4.3,4.8,4.1,4.7};
int distance[]= {500,1000,200,700,430};
}
public class selection extends drivers{
String d;
String cm;
int ds; 
int si;
void select(String carmode){
	int c=0;
	for(int i=0;i<5;i++) {
		if(super.carmodel[i].equals(carmode) && super.rating[i]>=4) {
			c=c+1;
			if(c==1){
				this.ds=super.distance[i];
				si=i;}
			if(c!=1 && super.distance[i]<this.ds) {
				this.ds=super.distance[i];
				this.si=i;
	}
}
}this.d=super.driver[si];}}
public class customerwork{
	public static void main(String[] args) {
		int klk;
		String s;
		System.out.println("This carmodels  are avilable for Ride rent Now:");
		System.out.println("Sedan"+"\nHatchBack"+"\nSeater");
		System.out.println("Customer Ride Distance :");
		Scanner sc = new Scanner(System.in);
		klk = sc.nextInt();
		System.out.println("Car Requested:");
		s =sc.next();
		selection selec=new selection();
		selec.select(s);
		System.out.println("Driver "+selec.d+" Will get you to the destintion.\n Your charge will be "+klk*8);
		
		sc.close();
	}
}
