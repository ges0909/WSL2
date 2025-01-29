# JDK and Maven

## JDK

```bash
sudo apt install -y openjdk-21-jdk
```

## Maven

```bash
wget https://dlcdn.apache.org/maven/maven-3/3.9.9/binaries/apache-maven-3.9.9-bin.tar.gz
gunzip apache-maven-3.9.9-bin.tar.gz
tar -xvf apache-maven-3.9.9-bin.tar
sudo mv apache-maven-3.9.9 /opt/maven
PATH="/opt/maven/bin:$PATH" # add to your ~/.profile
mvn --version # check installation
```
