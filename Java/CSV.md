# CSV


## Read csv with bufferedReader

```JAVA
public static void main(String[] args) throws IOException {
		// TODO Auto-generated method stub
		File file = new File("src/main/resources/data.csv");
		BufferedReader csvReader = new BufferedReader(new FileReader(file));

		String line = csvReader.readLine();
		while ((line = csvReader.readLine()) != null) {
			System.out.println(line);
		}
	}
```
## Simple reader into object
```JAVA
ArrayList<User> users = new ArrayList();
		
File file = new File("src/main/resources/data.csv");
BufferedReader csvReader = new BufferedReader(new FileReader(file));String line = csvReader.readLine();
while ((line = csvReader.readLine()) != null) {
	String[] User = line.split(",");
	System.out.println(User[0] + User[1] + User[2]);
	users.add(new User(User[2], User[1], Integer.parseInt(User[0])));
}

System.out.println(users.toString());
	
```

## Read CSV using CSVParser
```JAVA
File csvData = new File("src/main/resources/data.csv");
FileReader reader = new FileReader(csvData);
		
CSVParser parser = CSVParser.parse(reader, CSVFormat.EXCEL);
		
for (CSVRecord record : parser) {
	System.out.println(record);
}
```

## Builder

```JAVA
public enum headers {
		userId, userName, userFirstName
	}
	public static void main(String[] args) throws IOException {
		// TODO Auto-generated method stub
		Reader reader = new FileReader(new File("src/main/resources/data.csv"));
		CSVFormat csvFormat = CSVFormat.Builder.create()
					.setHeader(headers.class)
					.setAllowMissingColumnNames(true)
					.build();
		
		Iterable<CSVRecord> records = csvFormat.parse(reader);
		Iterator<CSVRecord> iterator = records.iterator();
		while(iterator.hasNext()) {
			System.out.println(iterator.next());
		}
	}
```


https://www.tutorialspoint.com/java-resultsetmetadata-getcolumntype-method-with-example