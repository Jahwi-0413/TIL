# 0130
- java create directory
- java file 저장

## javas create directory
```java
  Path path = Paths.get(pathString);

  //상위 폴더가 없으면 NoSuchFileException, 이미 폴더가 있으면 FileAlreadExistsException
  Files.createDirectory(path);

 //상위 폴더가 없으면 생성, 이미 폴더가 있어도 오류 X
  Files.createDirectories(path);  
```

## java file 저장
```java
MultiPartFile mfile;    //form-data에서 받아왔다고 가정

File file = new File(pathString);   //확장자까지 포함할것, 저장하려는 경로가 존재해야함
file.createNewFile();

FileOutputStream fos = new FileOutputStream(file);
fos.write(mfile.getBytes());
fos.close();
```
