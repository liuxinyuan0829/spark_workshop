# spark_workshop

Creating the Spark session works, but reading a file triggers Hadoop filesystem code that is not yet compatible with Java 25 in your environment.

Fix

Use Java 17 or Java 21 instead of Java 25. That is the correct fix. Spark’s official docs list 17/21, not 25.

In Codespaces:

sudo apt-get update
sudo apt-get install -y openjdk-17-jdk
export JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64
export PATH="$JAVA_HOME/bin:$PATH"
java -version