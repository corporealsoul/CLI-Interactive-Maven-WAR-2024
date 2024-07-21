anup@automation-and-continuous-delivery:~$ java --version
anup@automation-and-continuous-delivery:~$ javac --version
anup@automation-and-continuous-delivery:~$ mvn --version

APT Installation,
anup@automation-and-continuous-delivery:~$ sudo apt install fontconfig openjdk-17-jre
anup@automation-and-continuous-delivery:~$ sudo apt install openjdk-17-jdk-headless
anup@automation-and-continuous-delivery:~$ readlink -f $(which java)
/usr/lib/jvm/java-17-openjdk-amd64/bin/java
anup@automation-and-continuous-delivery:~$ sudo nano ~/.bashrc
#JAVA_HOME
export JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64
export PATH="$PATH:$JAVA_HOME/bin"

anup@automation-and-continuous-delivery:~$ source ~/.bashrc
anup@automation-and-continuous-delivery:~$ echo $JAVA_HOME
anup@automation-and-continuous-delivery:~$ echo $PATH
anup@automation-and-continuous-delivery:~$ java --version
anup@automation-and-continuous-delivery:~$ javac --version

anup@automation-and-continuous-delivery:~$ sudo apt-get update
anup@automation-and-continuous-delivery:~$ sudo apt install maven -y
anup@automation-and-continuous-delivery:~$ mvn -version
anup@automation-and-continuous-delivery:~$ readlink -f $(which mvn)
/usr/share/maven/bin/mvn
anup@automation-and-continuous-delivery:~$ sudo nano ~/.bashrc
#M2_HOME
export M2_HOME=/usr/share/maven
export PATH="$PATH:$M2_HOME/bin"

anup@automation-and-continuous-delivery:/opt$ source ~/.bashrc
anup@automation-and-continuous-delivery:/opt$ echo $M2_HOME
anup@automation-and-continuous-delivery:/opt$ echo $PATH
anup@automation-and-continuous-delivery:/opt$ mvn --version






Manual Installation,
https://www.oracle.com/java/technologies/downloads/
anup@automation-and-continuous-delivery:~$ wget https://download.oracle.com/java/21/latest/jdk-21_linux-x64_bin.deb
anup@automation-and-continuous-delivery:~$ sudo dpkg -i jdk-21_linux-x64_bin.deb
anup@automation-and-continuous-delivery:~$ sudo update-alternatives --config 'java'
anup@automation-and-continuous-delivery:~$ sudo update-alternatives --config 'javac'
anup@automation-and-continuous-delivery:~$ readlink -f $(which java)
anup@automation-and-continuous-delivery:~$ sudo nano ~/.bashrc
#JAVA_HOME
export JAVA_HOME=/usr/lib/jvm/jdk-21.0.4-oracle-x64
export PATH="$PATH:$JAVA_HOME/bin"

anup@automation-and-continuous-delivery:~$ source ~/.bashrc
anup@automation-and-continuous-delivery:~$ echo $JAVA_HOME
anup@automation-and-continuous-delivery:~$ echo $PATH
anup@automation-and-continuous-delivery:~$ java --version
anup@automation-and-continuous-delivery:~$ javac --version

https://maven.apache.org/download.cgi
anup@automation-and-continuous-delivery:~$ cd /opt/
anup@automation-and-continuous-delivery:/opt$ sudo wget https://dlcdn.apache.org/maven/maven-3/3.9.8/binaries/apache-maven-3.9.8-bin.tar.gz
anup@automation-and-continuous-delivery:/opt$ sudo tar -xvzf apache-maven-3.9.8-bin.tar.gz
anup@automation-and-continuous-delivery:/opt$ sudo nano ~/.bashrc
#M2_HOME
export M2_HOME=/opt/apache-maven-3.9.8
export PATH="$PATH:$M2_HOME/bin"

anup@automation-and-continuous-delivery:/opt$ source ~/.bashrc
anup@automation-and-continuous-delivery:/opt$ echo $M2_HOME
anup@automation-and-continuous-delivery:/opt$ echo $PATH
anup@automation-and-continuous-delivery:/opt$ mvn --version







anup@automation-and-continuous-delivery:~$ git clone https://github.com/corporealsoul/CLI-Interactive-Maven-WAR-2024.git
anup@automation-and-continuous-delivery:~$ mvn archetype:generate
2163: remote -> org.apache.maven.archetypes:maven-archetype-webapp (An archetype which contains a sample Maven Webapp project.)
Define value for property 'groupId': com.cliinteractivemavenwar2024
Define value for property 'artifactId': CLI-Interactive-Maven-WAR-2024
Define value for property 'version' 1.0-SNAPSHOT: : 1.0-SNAPSHOT
Define value for property 'package' com.cliinteractivemavenwar2024: : com.cliinteractivemavenwar2024.app
Confirm properties configuration:
groupId: com.cliinteractivemavenwar2024
artifactId: CLI-Interactive-Maven-WAR-2024
version: 1.0-SNAPSHOT
package: com.cliinteractivemavenwar2024.app
 Y: : Y

Maven build lifecyle :
anup@automation-and-continuous-delivery:~$ cd CLI-Interactive-Maven-WAR-2024/
Validate : anup@automation-and-continuous-delivery:~/CLI-Interactive-Maven-WAR-2024$ mvn validate
Compile : anup@automation-and-continuous-delivery:~/CLI-Interactive-Maven-WAR-2024$ mvn compile
Test : anup@automation-and-continuous-delivery:~/CLI-Interactive-Maven-WAR-2024$ mvn test
Package : anup@automation-and-continuous-delivery:~/CLI-Interactive-Maven-WAR-2024$ mvn package
Verify : anup@automation-and-continuous-delivery:~/CLI-Interactive-Maven-WAR-2024$ mvn verify
Install : anup@automation-and-continuous-delivery:~/CLI-Interactive-Maven-WAR-2024$ mvn install
Deploy




Maven Dependencies,
https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html
https://mvnrepository.com/