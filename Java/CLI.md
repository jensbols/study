```JAVA
public class MainCli {

	private DomainController dc;
	static Scanner s = new Scanner(System.in);

	public MainCli(DomainController dc) {
		this.dc = dc;
	}

	public void run() {
		boolean running = true;
		while(running) {
			System.out.println("1: optie");
			System.out.println("2: optie2");
			System.out.println("0: Exit");
			System.out.print("Choice:");
			
			switch(s.nextInt()) {
			case 1:
				method();
				break;
			case 2:
				method2();
				break;
			case 0:
				running = false;
				System.out.println("Application closed");
				System.exit(0);
				break;
			}
		}
	}
	
	private void writeToDialog() {
		System.out.print("Table name:");
		String tableName = s.next();
		System.out.print("CSV FilePath:");
		String path = s.next();
		
		dc.readCsvToDb(new File(path), tableName);
		
		
	}
	
	private void writeFromDialog() {
		System.out.print("Table name:");
		String tableName = s.next();
		
		System.out.print("CSV FilePath:");
		String path = s.next();
		
		dc.writeToCsvFromDb(new File(path), tableName);
		
	}
```