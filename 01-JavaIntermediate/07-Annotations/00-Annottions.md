# Annotations

In Java, annotations are a type of metadata that can be added to source code to provide additional information about the code. Annotations can be used to provide information such as documentation, code generation instructions, and compile-time error checking.

Annotations are denoted by the @ symbol followed by the name of the annotation. Annotations can be applied to classes, methods, fields, and other program elements.

Here's an example of using annotations in Java:

```
// declaring an annotation
@interface MyAnnotation {
    String value();
}
```

// using the annotation
@MyAnnotation("This is my annotation")
public class MyClass {
    // code here
}
In this example, we first declare an annotation MyAnnotation using the @interface keyword. The annotation has a single parameter value of type String.

We then apply the annotation to a class MyClass using the @ symbol followed by the name of the annotation and the parameter value. The annotation provides additional information about the class.

Annotations can be processed at runtime using reflection, or at compile time using annotation processing tools. Annotations are a powerful feature of Java that provide a way to add metadata to code and automate various tasks.