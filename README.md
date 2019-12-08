# Homework2
TextClock Tutorial

Introduction
  In android, TextClock is a UI control which is used to show the current date or time as a formatted string. The TextClock provides a date/time in two formats. One is to show the date/time in 24 Hour format and another is to show the date/time in 12 Hour format. In this tutorial, we will be using the TextClock as a 12 Hour format. This blog will explain what TextClock is about, the history of TextClock and what the attributes and methods mean. The app will be written in Java and XML. To display a TextClock alone, we do not need to add any methods in the MainActivity.java file. All we need is the attributes in the xml file. To display the time zone, some methods would be needed in the MainActivity.java file. We can also show how to use the time zone in this tutorial since that attribute comes under the category of TextClock.

History
  The TextClock has been introduced to android in API Level 17. If we use TextClock in our app it will require a minimum of API Level 17. If the app SDK version is lower than 17 then the TextClock will throw an error. It will display something like “View Required API Level 17”.

The major methods/attributes
  There are many methods and attributes that can be used for an android TextClock. It can be android:format12Hour, android:format24Hour, or android:timeZone. Some public methods that can be used for a TextClock program can be getDefault(), getDisplayName, and getID. These are the major methods and attributes used in this tutorial. The attributes are used in the xml file, and methods are used in the java file. I will explain more in depth what these attributes and methods mean.

   Android:format12Hour specifies the formatting pattern used to show the time and/or date in a 12 Hour mode. The default pattern for this attribute is in “h:mm:a”, which is a string used in java for date-time formatting. The “h” is for hour, the “mm” for minutes and the parameter “a” changes the hour part from the 24-Hour clock to the 12-Hour clock and adds an “am” or “pm".  If we were to use the 24 hour mode, the default pattern would be in “H:mm”.
 
  Android:timeZone is an attribute that specifies the time zone to be used. When this attribute is specified, the TextClock will ignore the time zone of the system. To use the users time zone, you do not have to specify this attribute. The default value is the users time zone. The time zone represents an offset and figures out daylight savings. 
You can get the TimeZone using the getDefault() method. This creates a time zone based on where the program is running. For example, a program running in Canada, getDefault creates a TimeZone object based on the Canadian standard time since the getDefault() method gets the default TimeZone for this host. The source of the default TimeZone may vary with implementation.

  The getDisplayName() method returns the short or long name of the time zone with either standard or daylight time, as written in locale. If the name is not available, the result is in the format GMT[+-]hh:mm. GMT stands for Greenwich Mean Time, also known as Universal Time. This method has the parameters of daylightTime, style, and locale. daylightTime is a boolean. True for daylight time, false for standard time. Style is used for an integer for either TimeZone#LONG or TimeZone#SHORT. Locale will display the local time. 

The Code
 In my android application, I have comments explaining what the major methods and attributes mean, and how they are organized to reach the results of running a TextClock in the app, along with the time zone. This will give you a better understanding on how to make a TextClock in android programming.
 
The reference
https://developer.android.com/reference/android/widget/TextClock
