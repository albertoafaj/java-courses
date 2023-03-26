In addition to the Scanner class, Java also provides the JOptionPane class, which is part of the javax.swing package, as an alternative way to input data. JOptionPane provides methods to display dialog boxes that prompt the user for input.

To use JOptionPane to read data from the user, you can use the showInputDialog method, which displays a dialog box with a prompt and an input field for the user to enter data. Here's an example:

```
import javax.swing.JOptionPane;

public class InputExample {
    public static void main(String[] args) {
        String name = JOptionPane.showInputDialog(null, "Enter your name:");
        JOptionPane.showMessageDialog(null, "Hello, " + name + "!");
        
        String ageString = JOptionPane.showInputDialog(null, "Enter your age:");
        int age = Integer.parseInt(ageString);
        JOptionPane.showMessageDialog(null, "You are " + age + " years old.");
    }
}

```

In this example, we use the showInputDialog method to display dialog boxes that prompt the user for their name and age. The showMessageDialog method is then used to display a message box with the user's name and age.

Note that the showInputDialog method returns a string, so we need to convert the age input to an integer using the Integer.parseInt method.

In summary, data input in Java can also be done using the JOptionPane class, which provides methods to display dialog boxes that prompt the user for input. The showInputDialog method is used to display the dialog box and return the input as a string.