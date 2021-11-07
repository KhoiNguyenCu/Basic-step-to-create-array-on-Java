# Basic-step-to-create-array-on-Java
I've learned basic steps to create (Array) today, so I want to practice and save my efforts here
public class Baitap10 {

	public Baitap10() {
		// TODO Auto-generated constructor stub
	}

  public static int enterN (Scanner scan) {
		int n; 
		do {
			System.out.println("Enter n >0 and n is even:\t");
			n = Integer.parseInt (scan.nextLine());
		}while (n<1 || n%2 !=0);
		return n;
	}
	
	public static int [] createArray (int n) {
		int a [] = new int [n];
		for (int i =0 ; i < n; i++) {
			a[i]=MIN +(int)(Math.random()* ((MAX - MIN) +1));
		}
		return a;
	}
	
	public static void exportArray (int a[]) {
		for (int item :a) {
			System.out.print(item + "\t");
		}
		System.out.println("\n");
	}
  
	public static void main(String[] args) {
		// TODO Auto-generated method stub
    Scanner scan = new Scanner (System.in);
		int n = enterN (scan);
		int a[]= createArray(n);
		exportArray(a);
	}

}
