# flink-sql-cook-on-zeppelin

## Introduction
This is [FLINK SQL Cookbook on Zeppelin] created for learning FLINK more conveniently
> more infomation about Zeppelin refer to [http://zeppelin.apache.org/]

## SetUp
### 1. Step 1, clone this project
```
git clone https://github.com/zjffdu/flink-sql-cookbook-on-zeppelin.git
```

### 2. Step 2, install Flink 1.12.1  

set $FLINK_HOME environment variable to the path of the uncompressed path

download website: https://flink.apache.org/downloads.html

### 3. Step 3, compile Flink faker 
compile and cope flink-faker-0.2.0.jar file to Flink's lib directory
download website: https://github.com/knaufk/flink-faker/
```
git clone https://github.com/knaufk/flink-faker/
cd flink-facker

// compile
mvn clean package

// copy jar file
cp ./target/flink-faker-0.2.0.jar $FLINK_HOME/lib

// check if copied success
ls $FLINK_HOME/lib
```

### 4. Step 4, Running, 
```
// start 
docker-compose up -d

// stop
docker-compose stop
```
after finished above visit http://localhost:8080/ and set FLINK_HOME to /flink in setting -> Interpreters -> search flink  
then restart flink interpreter and begin test flink jobs ...
