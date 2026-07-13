# Generation Process

## Project purpose
This project generates a java and typescript model based on the provided openapi.yaml file.
Both artifacts will be uploaded and shared in a public artifact repository.


## OpenAPI spec modification
If the openapi yaml changes → both generators reset to version 1. Generation will happen if 
proper release is triggered through github release. The release should have the openapi version only.
Version correlation is aggregated in this document. 

### Java generator modification
The Java generator code is updated (`java/`)
Java version suffix increments: +java.X → +java.X+1 in pom.xml
TypeScript version remains unchanged

### TypeScript generator modification
The TypeScript generator code is updated (`js/`)
TypeScript version suffix increments: +ts.X → +ts.X+1 in package.json
Java version remains unchanged
Version update in artifacts

### Git commit and tag
Tag: 
```
git tag v1.x.x-lang.x
```

### Version aggregation
Here is the version aggregator where you can find and correlated openapi, java and typescript version 
You can write any addition details in the comments section, which relates to the version constellation. 
For example, if there is a java only build, you can write where the newer version purpose.

| Openapi version | Java version | Typescript version | Comment |
|-----------------|--------------|--------------------|---------|
| 0.0.1           | 0.0.1+java.1 | 0.0.1+java.1       | N/A     |
