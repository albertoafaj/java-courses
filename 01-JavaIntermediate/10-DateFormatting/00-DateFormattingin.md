# Date Formattingin

In Java, date formatting allows you to convert a date object into a string representation using a specified format. This is useful when working with dates in different formats, such as displaying a date in a human-readable format or converting a date to a specific format for data exchange.

Here's an example of using date formatting in Java:

```
// creating a date object
Date date = new Date();

// creating a date format object
SimpleDateFormat dateFormat = new SimpleDateFormat("yyyy-MM-dd");

// formatting the date object
String formattedDate = dateFormat.format(date);

// outputting the formatted date
System.out.println("Formatted date: " + formattedDate);

```

In this example, we first create a Date object representing the current date and time. We then create a SimpleDateFormat object with the desired format pattern "yyyy-MM-dd", which represents the year, month, and day in a specific order.

We then use the format() method of the SimpleDateFormat object to format the Date object into a string representation using the specified format. Finally, we output the formatted date to the console.

There are many different date format patterns that can be used with the SimpleDateFormat class, allowing for a wide range of date formatting options. Date formatting in Java is a powerful tool that can be used to manipulate dates in a variety of ways.

### Calender

In Java, the Calendar class is used to work with dates and times. It provides many methods for manipulating dates, such as adding or subtracting time intervals, setting specific date and time values, and formatting dates and times.

Here's an example of using the Calendar class and some of its methods:

```
// creating a calendar instance
Calendar cal = Calendar.getInstance();

// getting the current date and time
Date currentDate = cal.getTime();
System.out.println("Current date and time: " + currentDate);

// setting a specific date and time
cal.set(Calendar.YEAR, 2023);
cal.set(Calendar.MONTH, Calendar.JULY);
cal.set(Calendar.DAY_OF_MONTH, 1);
cal.set(Calendar.HOUR_OF_DAY, 13);
cal.set(Calendar.MINUTE, 30);
cal.set(Calendar.SECOND, 0);
cal.set(Calendar.MILLISECOND, 0);

// adding a time interval
cal.add(Calendar.DAY_OF_MONTH, 7);
cal.add(Calendar.HOUR_OF_DAY, 2);
cal.add(Calendar.MINUTE, 30);

// getting the updated date and time
Date updatedDate = cal.getTime();
System.out.println("Updated date and time: " + updatedDate);

// formatting the date and time
SimpleDateFormat dateFormat = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");
String formattedDate = dateFormat.format(updatedDate);
System.out.println("Formatted date and time: " + formattedDate);

```

In this example, we first create a Calendar object using the getInstance() method, which returns a Calendar instance initialized to the current date and time in the default time zone and locale.

We then use the getTime() method to get the current date and time as a Date object, and output it to the console.

Next, we use the set() method to set a specific date and time, with the year 2023, month of July, and day of the month 1, at 1:30 PM. We also set the milliseconds to 0.

We then use the add() method to add 7 days, 2 hours, and 30 minutes to the current date and time.

Finally, we use the getTime() method to get the updated date and time as a Date object, and format it using a SimpleDateFormat object with the format pattern "yyyy-MM-dd HH:mm:ss". We then output the formatted date and time to the console.

The Calendar class provides many other methods for working with dates and times, such as get(), roll(), and clear(), allowing for a wide range of date and time manipulation options.