# java-sizeof
a simple class, used to calculate java Object size, implemented by JDK above 1.5, resolved the manifest.mf file add pre-class attr problem
. origin doc refer https://www.baeldung.com/java-size-of-object

# quickStart
  1.clone code & build in your maven repository<br>
  2.import this jar file to your maven project by pom.xml<br>
  3.config run/debug arguments, add -javaagent:"ClassPath\InstrumentationAgent-0.0.1-SNAPSHOT.jar" to VM Options<br>
  4.import cn.com.instrument.InstrumentationAgent;<br>
  5.insert ref code:<br>
  
  ```java
  public static void printObjectSize(Object object) {
        System.out.println("Object type: " + object.getClass() +
          ", size: " + InstrumentationAgent.getObjectSize(object) + " bytes");
    }
    
  6.start run/debug
  
