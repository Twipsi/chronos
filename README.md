# Chronos
 Simple class to play with time

## Initializing the class

 You can set the initial date as a DateTime object or a valid date string or a timestamp.

 ```php
 Chronos::date(new DateTime)
 Chronos::date('2022-05-05 10:10:10')
 Chronos::date(1664524279)
 ```

 ## DateTime Options

 You can specify each option fluently after setting the initial date.

  ```php
 Chronos::date($date)
    ->setDateTimeFormat("Y-m-d H:i:s")
    ->setDateFormat("Y-m-d")
    ->setTimeFormat("H:i:s")
    ->setTimezone("UTC")
 ```

## Retrieving the datetime as a string

  You have multiple methods to retrieve the datetime as a string.

```php
 Chronos::date($date)->getDateObject()
    || ->stamp()
    || ->getDateTime()
    || ->getDate()
    || ->getTime()
    || ->getHour()
    || ->getMinute()
    || ->getSeconds()
    || ->getDayName()
    || ->getDayShortName()
    || ->getDayNumber()
    || ->getWeekNumber()
    || ->getMonthName()
    || ->getShortMonthName()
    || ->getMonthNumber()
    || ->getYear()
 ```

## Manipulating datetime

### Initial methods

  You have several methods to manipulate the initial time before retrieving it as a string.

  ```php
 Chronos::date($date)->addDays()->getDateTime();
 Chronos::date($date)->addMinutes()->getDateTime();
 Chronos::date($date)->addSeconds()->getDateTime();
 Chronos::date($date)->subDays()->getDateTime();
 Chronos::date($date)->subMinutes()->getDateTime();
 Chronos::date($date)->subSeconds()->getDateTime();
 ```

### Chaining methods

 You can also chain the methods fluently.

   ```php
 Chronos::date($date)->addDays(40)->addMinutes(1)->subSeconds(20)->getDateTime();
 ```

 ### Traveling in time