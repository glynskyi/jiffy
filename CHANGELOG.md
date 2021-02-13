## 4.0.0-nullsafety

- Major changes

Opt in the null safety

## 3.0.1

- Patch changes

Fixed `Undefined name 'Units'` bug

Swedish locale `sv` contributed by [Erik Carlsson](https://github.com/ercadev)

## 3.0.0

- Major changes

Unit of time are now in enums. Examples, previously `startOf("day")` can now be set as `startOf(Units.DAY)`
String escape changes to use square braces `[]`. Examples, previously
 
`Jiffy().format("yyyy 'escaped' yyyy");` and now updated to `Jiffy().format("yyyy [escaped] yyyy");`

Added Indonsia local `id` by [ampersanda](https://github.com/ampersanda) and Turkish local `tr` by [iozozturk](https://github.com/iozozturk)


## 2.2.0

- Added more string parsing functionality. See below

```
Jiffy("1995/12/25"); // A calendar date part separated by slash "/"
Jiffy("19951225"); // Basic (short) full date
Jiffy("1995-12-25 12:00:00.000"); // An hour, minute, second, and millisecond time part
Jiffy("1995-12-25T12:00:00.000"); ISO dart format
Jiffy("1995-12-25T12:00:00.000Z"); ISO dart format (UTC)
```

- Added support to Polish locale `pl` added by [leszekkrol](https://github.com/leszekkrol)

## 2.1.2

- Minor bug fixes on the following

Bug fix to support `startOf` and `endOf` for locales

Bug fix on week getter

By [MrCasCode](https://github.com/MrCasCode)

## 2.1.1

- Minor bug fixes on ordinal date formating

Previously

`Jiffy([2014, 4, 23]).format("EEEE MMMM do, yyyy"); // Wednesday April 23o, 2014`

Updated

`Jiffy([2014, 4, 23]).format("EEEE MMMM do, yyyy"); // Wednesday April 23rd, 2014`

## 2.1.0

- Ordinal date parsing and formating
In Jiffy you can now parse and format with ordinal date. e.g
```dart
Jiffy().format("MMM do yyyy"); // Oct 19th 2019
```
- It also supports locales for the following

`"en", "es", "fr", "frch", "frca", "it", "itch", "ja", "ko", "pt", "ptbr", "zh", "zhcn", "zhhk", "zhtw", "de", "deat", "dech"`

- Added `daysInMonth` method to get number of days for specific months .e.g
```dart
Jiffy([2016, 1]).daysInMonth; // 31
Jiffy([2016, 2]).daysInMonth; // 28
Jiffy([2017, 2]).daysInMonth; // 29
```

## 2.0.0

Added params to add and subtract methods by [yongjhih](https://github.com/yongjhih)
Example
```dart
Jiffy().add(days: 1);
Jiffy().add(years: 2, months: 1, duration: Duration(days: 1, hours: 30));
```

## 1.1.0

Add more functionality to parsing. These are
- Array parsing `Jiffy([2019, 10, 21]);`
- Map parsing `Jiffy({"year": 2019, "month": 10});`
- Dart DateTime parsing `Jiffy(DateTime.now());`
- String parsing `Jiffy("2019-10-21");`

## 1.0.0

- Initial version, created by Stagehand
