## csv 파일 리더


### pom.xml
```xml
<dependency>
  <groupId>com.opencsv</groupId>
  <artifactId>opencsv</artifactId>
  <version>5.5.2</version>
</dependency>
```

### java 파일
```java
public List<String[]> readCsv(String fileName) {
  List<String[]> records = new ArrayList<>();
  Resource resource = new ClassPathResource(fileName);

  try (CSVReader csvReader = new CSVReader(new InputStreamReader(resource.getInputStream()))) {
    String[] values;
    while ((values = csvReader.readNext()) != null) {
      records.add(values);
    }
  } catch (Exception e) {
    log.error(e.getMessage());
  }
  return records;
}
```

