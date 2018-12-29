# bookstore-modularized
A simple application with new features of java 9+ new modularized. (JDK version used: jdk 11)

how to compile: 

  DOMAIN MODULE
  
  javac -d mods/br.com.casadocodigo.domain --module-path mods/ src/br.com.casadocodigo.domain/module-info.java 
      src/br.com.casadocodigo.domain/br/com/casadocodigo/model/\*.java
      
  HTTP MODULE    
  
  javac -d mods/br.com.casadocodigo.http --module-path mods/ src/br.com.casadocodigo.http/module-info.java 
      src/br.com.casadocodigo.http/br/com/casadocodigo/data/\*.java
      
  NF MODULE(REACTIVE STREAM)    
  
  javac -d mods/br.com.casadocodigo.nf --module-path mods/ src/br.com.casadocodigo.nf/module-info.java 
      src/br.com.casadocodigo.nf/br/com/casadocodigo/nf/internal/\*.java 
      src/br.com.casadocodigo.nf/br/com/casadocodigo/nf/model/\*.java
      src/br.com.casadocodigo.nf/br/com/casadocodigo/nf/service/\*.java
  
  MAIN MODULE
  
  javac -d mods/br.com.casadocodigo --module-path mods/ src/br.com.casadocodigo/module-info.java 
      src/br.com.casadocodigo/br/com/casadocodigo/Main.java
      
how to run: 
   java --module-path mods -m br.com.casadocodigo/br.com.casadocodigo.Main
