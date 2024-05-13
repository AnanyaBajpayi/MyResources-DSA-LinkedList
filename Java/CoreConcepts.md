-Interface:Apply some rules on methods
-public interface Phone {
	String processor();
	String OS();
	int spaceInGB();
}
-public class Iphone8 implements Phone{

	@Override
	public String processor() {
		
		return "A11";
	}

	@Override
	public String OS() {
		
		return "IOS";
	}

	@Override
	public int spaceInGB() {
		
		return 64;
	}

}
-public class OnePlus5 implements Phone{

	@Override
	public String processor() {
		
		return "SD835";
	}

	@Override
	public String OS() {
		
		return "Android";
	}

	@Override
	public int spaceInGB() {
		
		return 64;
	}
	
}