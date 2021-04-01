The default option that requires **no installation** would be to use the `file` command. For our code example we will work with files from the [General Example Files](https://www.nih-cfde.org/resource/Example_data_files.md).

#### Usage
```
file --mime-type <name of the file>
```

#### Input
```
file --mime-type 6285633006_R03C01_Red.idat
```

#### Expected Output
```
6285633006_R03C01_Red.idat: application/octet-stream
```

Adding the `-b` flag returns only the MIME type for the selected file without the filename.

#### Input
```
file --mime-type -b 9969477031_R02C01_Red.idat
```

#### Expected Output
```
application/octet-stream
```
