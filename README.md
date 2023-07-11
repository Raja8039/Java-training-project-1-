# Java-training-project-1-
    import java.util.*;
    import java.text.DecimalFormat;
    public class Currency_converter {
	double rupee,dollar,pound,euro,code;
	DecimalFormat f=new DecimalFormat("##.###");
	Scanner ab=new Scanner(System.in);
	public void converter1() {
		System.out.println("Enter your amount in Rupees:");
		rupee=ab.nextFloat();
		dollar=rupee/75;
		System.out.println("Dollar:"+f.format(dollar));
		pound=rupee/101;
		System.out.println("Pound:"+f.format(pound));
		euro=rupee/84;
		System.out.println("Euro:"+f.format(euro));
	}
	public void converter2() {
		System.out.println("Enter your amount in Dollars:");
		dollar=ab.nextFloat();
		rupee=dollar*75;
		System.out.println("Rupee:"+f.format(rupee));
		pound=dollar*0.72;
		System.out.println("Pound:"+f.format(pound));
		euro=dollar*0.88;
		System.out.println("Euro:"+f.format(euro));
	}
	public void converter3() {
		System.out.println("Enter your amount in Pound:");
		pound=ab.nextFloat();
		dollar=pound*1.35;
		System.out.println("Dollar:"+f.format(dollar));
		rupee=pound*101;
		System.out.println("Rupee:"+f.format(rupee));
		euro=pound*1.36;
		System.out.println("Euro:"+f.format(euro));
	}
	public void converter4() {
		System.out.println("Enter your amount in Euro:");
		euro=ab.nextFloat();
		dollar=euro*1.12;
		System.out.println("Dollar:"+f.format(dollar));
		pound=euro*0.73;
		System.out.println("Pound:"+f.format(pound));
		rupee=euro*84;
		System.out.println("Rupee:"+f.format(rupee));
	}

	public static void main(String[] args) {
		Currency_converter x=new Currency_converter();
		System.out.println("Select your Currency Code\n1:Rupee\n2:Dollar\n3:Pound\n4:Euro\nEnter your code:");
		Scanner ab=new Scanner(System.in);
		int code=ab.nextInt();
		if (code==1) {
			x.converter1();
		}
		else if (code==2) {
			x.converter2();
		}
		else if (code==3) {
			x.converter3();
		}
		else if (code==4) {
			x.converter4();
		}
		System.out.println("Thank You!");

	}

}
