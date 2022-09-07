# HyperFrame-Kafka
- 업로드된 바이너리는 HyperFrame Kafka 제품 설치를 위한 파일

## 설치파일
### zookeeper
* Version : apache-zookeeper-3.8.0-bin.tar.gz
* Note : https://dlcdn.apache.org/zookeeper/zookeeper-3.8.0/apache-zookeeper-3.8.0-bin.tar.gz
* 설명

### kafka
* Version : kafka_2.12-3.2.1.tgz
* Note : https://downloads.apache.org/kafka/3.2.1/
* 설명

## Kafka 지원 Java Version
* 

## 검증환경
* Centos Linux release 7.9.2009

## 설치 및 실행

### 1) zookeeper 설치 및 압축풀기

    $ cd ${INSTALLER_HOME}
    $ tar -zxf apache-zookeeper-3.8.0-bin.tar.gz
    
### 2) zookeeper 환경설정

    $ cd ${ZOOKEEPER_HOME}/conf
    $ cp zoo_sample.cfg zoo.cfg
    ...
    tickTime=2000
    initLimit=10
    syncLimit=5
    dataDir=${ZOOKEEPER_HOME}/.data/zookeeper
    clientPort=2181
    ...
    
### 3) zookeeper 실행
 
     $ cd ${ZOOKEEPER_HOME}/bin
     $ ./zkServer.sh start
     
### 4) zookeeper cli 명령어 실행 테스트
     $ [zk: localhost:2181(CONNECTED) 0] ls /
     $ [zookeeper] 
