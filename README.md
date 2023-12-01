## Multi-module Project Sructure
```
ShopmeProject
    |____shopmecomon
    |____shopmewebparent(simple maven project)
                |____shopmebackend
                |____shopmefrontend
```

### problems 

#### for creating multi-module spring project

1. make sure the parent project pom file adds these labels

```
    <packaging>pom</packaging>
    <modules>
        <module>childprojectName</module>
    </modules>
```

2. for child project, change the parent label according to parent pom.xml file
```
    # this is shopmewebparent pom.xml
    <parent>
        <groupId>com.shopme</groupId>
        <artifactId>ShopemeProject</artifactId>   
        <version>0.0.1-SNAPSHOT</version>
    </parent>
```

#### if using vscode, may encounter issue that extension cannot used

    move the project to C Disk

## build project
```
    # in root folder which is shopemeproject folder
    mvn install
```