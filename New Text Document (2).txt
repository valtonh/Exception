//import java.util.ArrayList;

public class ExceptionExample1 {
	public static void main(String[] args) {
		
		foo();
		try {
			bar();
			//8
			//throw new IndexOutOfBoundsException();	

		} catch (IndexOutOfBoundsException iobe) {
			System.out.println("ERROR 1");
		} catch (ArithmeticException ae) {
			System.out.println("ERROR 2");
		} finally {
			System.out.println("DONE");
		}
	}

	public static void foo() {
		//A
		// ArrayList<Integer> numbers = new ArrayList<Integer>();
		// System.out.println(numbers.get(0));
		
		//ClassCastException
		/*Object i = Integer.valueOf(42);
		String s = (String)i; */
		try {
			//B
			// int a = 1 / 0;
		} catch (NullPointerException npe) {
			System.out.println(npe.getMessage());
			npe.printStackTrace();
		}
	}

	public static void bar() {
		//C
		// int a = Integer.parseInt("a");
		try {
			// PROGRAM LINE D
			methodX();
		} catch (NullPointerException npe) {
			System.out.println("ERROR 3");
		} catch (IndexOutOfBoundsException iobe) {
			System.out.println("ERROR 4");
		}
		System.out.println("DONE BAR");
	}

	public static void methodX() {
		//E
		/*String a = null, b = "Hello";
		if (a.equals(b));
		System.out.println("Equals");*/
		
		
		try {
			
			//F
			//ArrayList<Integer> nr = new ArrayList<Integer>();
			//nr.add(1, 5);
			} catch (IndexOutOfBoundsException iobe) {
			System.out.println(iobe.getMessage());
			iobe.printStackTrace();
		} catch (NumberFormatException nfe) {
			System.out.println("ERROR 5");
			return;
		} finally {
			System.out.println("DONE METHODX");
		}
	}
}
