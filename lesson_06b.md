#### Abstract class

``````java
package org.example;

public abstract class People {

    String firstName;

    String lastName;
    
    public String getFullName(){
        return lastName + firstName;
    }

}
``````
