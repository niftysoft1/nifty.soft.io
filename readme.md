## Nitfy tool 

This tool allows you to convert properties files to YAML format and YAML files to properties format.

## Prerequisites

- Intelij Version ()


## Plugin - Features

### 1. Properties to Yaml

Input: sample.properties
```
#Thu Apr 11 17:37:58 SRET 2019
db.user=mkyong
db.password=password
db.url=localhost
fValue=1.2
iValue=100
sValue=Hello world
yamlconfig.list[0]=item1
yamlconfig.list[1]=item2
yamlconfig.list[2]=item3
yamlconfig.list[3]=item4
```
Output: sample.yaml
```
db:
  user: mkyong
  password: password
  url: localhost
sValue: Hello world
yamlconfig:
  list:
  - item1
  - item4
  - item3
fValue: '1.2'
iValue: '100'
```

### 2. Yaml To Properties 

Input: yaml_input.yaml
```
application:
  props:
    name: YamlList
    url: http://yamllist.dev
    description: "Mapping list in Yaml to list of objects in Spring Boot"
    ips:
    -
      ip: 10.10.10.10
      port: 8091
    -
      email: support@yamllist.dev
      contact: http://yamllist.dev/contact
  users:
    -
      username: admin
      password: admin@10@
      roles:
        - READ
        - WRITE
        - VIEW
        - DELETE
    -
      username: guest
      password: guest@01
      roles:
        - VIEW
  profiles:
    - dev
    - test
    - prod
    - 1
    - 2
  list:
    - item1
    - item2
    - item3
    - item4
```
Output: yaml_output.yaml
```
#Wed Jun 07 20:09:59 ICT 2023
application.list[0]=item1
application.list[1]=item2
application.list[2]=item3
application.list[3]=item4
application.profiles[0]=dev
application.profiles[1]=test
application.profiles[2]=prod
application.profiles[3]=1
application.profiles[4]=2
application.props.description=Mapping list in Yaml to list of objects in Spring Boot
application.props.ips[0].ip=10.10.10.10
application.props.ips[0].port=8091
application.props.ips[1].contact=http\://yamllist.dev/contact
application.props.ips[1].email=support@yamllist.dev
application.props.name=YamlList
application.props.url=http\://yamllist.dev
application.users[0].password=admin@10@
application.users[0].roles[0]=READ
application.users[0].roles[1]=WRITE
application.users[0].roles[2]=VIEW
application.users[0].roles[3]=DELETE
application.users[0].username=admin
application.users[1].password=guest@01
application.users[1].roles[0]=VIEW
application.users[1].username=guest
```
### 3. XML To JSON


# Contributing

Contributions are welcome! If you have any ideas, suggestions, or bug reports, please open an issue or submit a pull request.

# License