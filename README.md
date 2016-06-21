# HelloWorldAnt
En ese repositorio vamos a:

* Crear un proyecto java (Hello World) con Apache Ant, para ayudarnos a la compilación, y los tests...
* Haremos una integración continua con Jenkins
* Seguiremos el tutorial oficial de Apache Ant: https://ant.apache.org/manual/tutorial-HelloWorldWithAnt.html

# Creamos el proyecto en el filesystem

training@ubuntu-devops:~/devops/repomartes$ more src/oata/HelloWorld.java
package oata;

public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello World");
    }
}
training@ubuntu-devops:~/devops/repomartes$

# Probamos

training@ubuntu-devops:~/devops/repomartes$ mkdir -p  build/classes
training@ubuntu-devops:~/devops/repomartes$ javac -sourcepath src -d build/classes src/oata/HelloWorld.java
training@ubuntu-devops:~/devops/repomartes$ java -cp build/classes oata.HelloWorld
Hello World
