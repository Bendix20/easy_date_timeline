<p align="center">
<a href="https://pub.dev/packages/easy_date_timeline"><img src="https://img.shields.io/pub/v/easy_date_timeline.svg" alt="Pub"></a>
<a href="https://github.com/FadyFayezYounan/easy_date_timeline/stargazers"><img src="https://img.shields.io/github/stars/FadyFayezYounan/easy_date_timeline?style=social" alt="GitHub stars"></a>
<a href="https://pub.dev/packages/easy_date_timeline/score"><img src="https://img.shields.io/pub/likes/easy_date_timeline?logo=flutter" alt="Pub likes"></a>
<a href="https://pub.dev/packages/easy_date_timeline/score"><img src="https://img.shields.io/pub/popularity/easy_date_timeline?logo=flutter" alt="Pub popularity"></a>
<a href="https://pub.dev/packages/easy_date_timeline/score"><img src="https://img.shields.io/pub/points/easy_date_timeline?logo=flutter" alt="Pub points"></a>
</p>

# EasyDateTimelinePicker

`EasyDateTimeLinePicker` is a customizable date and time picker widget for Flutter applications. It provides a horizontal timeline interface for selecting dates, with various customization options for appearance and behavior.

![Easy Date Timeline Picker](https://raw.githubusercontent.com/FadyFayezYounan/easy_date_timeline/master/screenshots/easy_date_timeline_picker.png)

## Contents

- [Getting Started](#getting-started)
- [Basic Usage](#basic-usage)

## Getting Started

Add the `easy_date_timeline` package to `pubspec.yaml`:

`flutter pub add easy_date_timeline`

Import the package to use it:

```dart
import 'package:easy_date_timeline/easy_date_timeline.dart';
```

## Basic Usage

# EasyDateTimeline

<a href="https://pub.dev/packages/easy_date_timeline"><img src="https://img.shields.io/pub/v/easy_date_timeline.svg" alt="Pub"></a>
<a href="https://pub.dev/packages/easy_date_timeline/score"><img src="https://img.shields.io/pub/likes/easy_date_timeline?logo=flutter" alt="Pub likes"></a>
<a href="https://pub.dev/packages/easy_date_timeline/score"><img src="https://img.shields.io/pub/popularity/easy_date_timeline?logo=flutter" alt="Pub popularity"></a>
<a href="https://pub.dev/packages/easy_date_timeline/score"><img src="https://img.shields.io/pub/points/easy_date_timeline?logo=flutter" alt="Pub points"></a>

The "easy_date_timeline" package is a customizable Flutter library that displays a timeline of dates in a horizontal view.

| Image Preview                                                                                                                           | Gif Preview                                                                                                                             |
| --------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| <img width="300" src="https://raw.githubusercontent.com/FadyFayezYounan/easy_date_timeline/master/screenshots/easy_date_timeline.jpg"/> | <img width="300" src="https://raw.githubusercontent.com/FadyFayezYounan/easy_date_timeline/master/screenshots/easy_date_timeline.gif"/> |

## 📦 Other Packages

- [easy_infinite_pagination](https://pub.dev/packages/easy_infinite_pagination) : The Easy Infinite Pagination package provides a simple and customizable way to implement infinite pagination in your Flutter applications.

- [flutter_easy_validator](https://pub.dev/packages/flutter_easy_validator): package designed to simplify the process of validating strings in your applications.

- [easy_radio](https://pub.dev/packages/easy_radio): EasyRadio is a customizable radio button widget for Flutter that offers consistent animation, easy customization of sizes, shape, inner dot shape.

# What's new?

- Add new widget called: `EasyInfiniteDateTimeLine` , It allows you to define a range of dates with `firstDate` and `lastDate`, specify the initial focus with `focusedDate`, and offers a `controller` for programmatic interactions:

`controller`: The Controller parameter is an optional controller that allows you to manage and interact with the InfiniteTimeLineWidget. You can use this controller to programmatically manipulate the widget's behavior. For example, you can scroll to specific dates, control animations, or perform other actions within the timeline. This controller is a powerful tool for integrating the widget with your app's logic.

`firstDate`: This required parameter specifies the start date of the timeline. It defines the earliest date that will be displayed in the timeline view. You should set this date to the beginning of the time range you want to visualize.

`lastDate`: This required parameter defines the end date of the timeline. It determines the latest date that will be visible within the timeline. Typically, this date should be set to represent the end of the time range you want to display.

`focusedDate`: Another required parameter, the focusedDate determines which date is currently in focus within the timeline.

## How To Use `EasyInfiniteDateTimeLine`

Import the following package in your dart file

```dart
import 'package:easy_date_timeline/easy_date_timeline.dart';
```

## Usage

Use the `EasyInfiniteDateTimeLine` Widget

```dart
 final EasyInfiniteDateTimelineController _controller =
      EasyInfiniteDateTimelineController();

        EasyInfiniteDateTimeLine(
          controller: _controller,
          firstDate: DateTime(2023),
          focusDate: _focusDate,
          lastDate: DateTime(2023, 12, 31),
          onDateChange: (selectedDate) {
            setState(() {
              _focusDate = selectedDate;
            });
          },
        ),
```

## How To Use `EasyDateTimeLine`

Import the following package in your dart file

```dart
import 'package:easy_date_timeline/easy_date_timeline.dart';
```

## Usage

Use the `EasyDateTimeLine` Widget

```dart
    EasyDateTimeLine(
      initialDate: DateTime.now(),
      onDateChange: (selectedDate) {
        //`selectedDate` the new date selected.
      },
    ),
```

## Features

- `Dynamic Text Color` : The "easy_date_timeline" package automatically adjusts the text color of the active day based on the active color. If the active color is a dark color, the text color will be light, and if the active color is a light color, the text color will be dark. This ensures that the text is always easy to read and contrasts well with the background color.
- `Customizable Item Builder` : The "easy_date_timeline" package provides an item builder that allows for full customization of the timeline items. With the item builder, developers can customize the appearance and behavior of each date item in the timeline, including the text, background color,etc..

  > **IMPORTANT NOTE:**
  >
  > When utilizing the `itemBuilder`, it is essential to provide the width of each day for the date timeline widget.
  >
  > For example:

  ```dart
   dayProps: const EasyDayProps(
    // You must specify the width in this case.
    width: 124.0,
   ),

  ```

- `Locale Support` : The "easy_date_timeline" package supports locale, allowing developers to display the timeline in different languages and formats based on the user's device settings. This feature ensures that the package can be used in a variety of international contexts and provides a seamless user experience for users around the world.

## `EasyInfiniteDateTimeLine` itemBuilder example:

You can use the `itemBuilder` to customize the appearance of the day widget.
The `itemBuilder` provides the following:

- `BuildContext context`: The context of the widget.
- `DateTime date`: The date of the day widget.
- `bool isSelected`: Whether the day widget is selected or not.
- `VoidCallback onTap`: The callback that triggers when the day widget is tapped.

<p>
 <img src="https://raw.githubusercontent.com/FadyFayezYounan/easy_date_timeline/master/screenshots/infinite_item_builder_example.jpg"/>
</p>

```dart
    return EasyInfiniteDateTimeLine(
      selectionMode: const SelectionMode.autoCenter(),
      firstDate: DateTime(2024),
      focusDate: _focusDate,
      lastDate: DateTime(2024, 12, 31),
      onDateChange: (selectedDate) {
        setState(() {
          _focusDate = selectedDate;
        });
      },
      dayProps: const EasyDayProps(
        // You must specify the width in this case.
        width: 64.0,
        // The height is not required in this case.
        height: 64.0,
      ),
      itemBuilder: (
        BuildContext context,
        DateTime date,
        bool isSelected,
        VoidCallback onTap,
      ) {
        return InkResponse(
          // You can use `InkResponse` to make your widget clickable.
          // The `onTap` callback responsible for triggering the `onDateChange`
          // callback and animating to the selected date if the `selectionMode` is
          // SelectionMode.autoCenter() or SelectionMode.alwaysFirst().
          onTap: onTap,
          child: CircleAvatar(
            // use `isSelected` to specify whether the widget is selected or not.
            backgroundColor:
                isSelected ? fillColor : fillColor.withOpacity(0.1),
            radius: 32.0,
            child: Column(
              mainAxisAlignment: MainAxisAlignment.center,
              children: [
                Flexible(
                  child: Text(
                    date.day.toString(),
                    style: TextStyle(
                      color: isSelected ? Colors.white : null,
                    ),
                  ),
                ),
                Flexible(
                  child: Text(
                    EasyDateFormatter.shortDayName(date, "en_US"),
                    style: TextStyle(
                      color: isSelected ? Colors.white : null,
                    ),
                  ),
                ),
              ],
            ),
          ),
        );
      },
    )
```

> [See also itemBuilder example for `EasyDateTimeLine`](#itemBuilder-example)

## Custom background

Use the `activeDayProps` in `dayProps` that contains decoration
for the active day.

<p>
 <img src="https://raw.githubusercontent.com/FadyFayezYounan/easy_date_timeline/master/screenshots/custom_background_example.jpg"/>
</p>

```dart
    EasyDateTimeLine(
      initialDate: DateTime.now(),
      onDateChange: (selectedDate) {
        //`selectedDate` the new date selected.
      },
      headerProps: const EasyHeaderProps(
        monthPickerType: MonthPickerType.switcher,
        dateFormatter: DateFormatter.fullDateDMY(),
      ),
      dayProps: const EasyDayProps(
        dayStructure: DayStructure.dayStrDayNum,
        activeDayStyle: DayStyle(
          decoration: BoxDecoration(
            borderRadius: BorderRadius.all(Radius.circular(8)),
            gradient: LinearGradient(
              begin: Alignment.topCenter,
              end: Alignment.bottomCenter,
              colors: [
                Color(0xff3371FF),
                Color(0xff8426D6),
              ],
            ),
          ),
        ),
      ),
    )
```

## Change current day highlight color and style

in the `dayProps` you can set `todayHighlightStyle` to :

- `TodayHighlightStyle.withBackground` : Set a background color for the current day.
- `TodayHighlightStyle.withBorder` : Set just a colored border for the current day.
- `TodayHighlightStyle.none` : Remove the highlight from the current day.
  by default the highlight color equal to primary color with opacity of 20%.
  to change the highlight color you can use `todayHighlightColor` and set your own color.

<p>
 <img src="https://raw.githubusercontent.com/FadyFayezYounan/easy_date_timeline/master/screenshots/change_today_highlight_color_and_style.jpg"/>
</p>

```dart
    EasyDateTimeLine(
      initialDate: DateTime.now(),
      onDateChange: (selectedDate) {
        //`selectedDate` the new date selected.
      },
      activeColor: const Color(0xff85A389),
      dayProps: const EasyDayProps(
        todayHighlightStyle: TodayHighlightStyle.withBackground,
        todayHighlightColor: Color(0xffE1ECC8),
      ),
    )
```

> **NOTE:**
> When you provide an `inactiveDay.decoration` to the EasyDateTimeline widget, it will override the current day highlight feature.

## Change day structure

In the `dayProps` change the `dayStructure` to:

- `DayStructure.dayNumDayStr` : show the current day number then current day name.
- `DayStructure.dayStrDayNum` : show the current name then current day number.
- `DayStructure.monthDayNumDayStr` : show current month name then the current day number finally current day name.
- `DayStructure.dayNumberOnly` : show only current day number.
- `DayStructure.dayNameOnly` : show only current day name.
- `DayStructure.dayStrDayNumMonth` : show current day name then the current day number finally current moth name.

<p>
 <img src="https://raw.githubusercontent.com/FadyFayezYounan/easy_date_timeline/master/screenshots/change_day_structure_example.jpg"/>
</p>

```dart
    EasyDateTimeLine(
      initialDate: DateTime.now(),
      onDateChange: (selectedDate) {
        //`selectedDate` the new date selected.
      },
      activeColor: const Color(0xffFFBF9B),
      headerProps: const EasyHeaderProps(
        dateFormatter: DateFormatter.monthOnly(),
      ),
      dayProps: const EasyDayProps(
        height: 56.0,
        width: 56.0,
        dayStructure: DayStructure.dayNumDayStr,
        inactiveDayStyle: DayStyle(
          borderRadius: 48.0,
          dayNumStyle: TextStyle(
            fontSize: 18.0,
          ),
        ),
        activeDayStyle: DayStyle(
          dayNumStyle: TextStyle(
            fontSize: 18.0,
            fontWeight: FontWeight.bold,
          ),
        ),
      ),
    )
```

## Locale support

With `easy_date_timeline`, you can display dates and timelines in your preferred language and format. Simply pass the locale parameter with the appropriate language code and region as a value. For example, if you want to display the dates in Arabic, you can set the locale parameter to "ar". The package's support for localization allows you to provide a better user experience for users around the world by displaying text and information in their preferred language and format.

<p>
 <img src="https://raw.githubusercontent.com/FadyFayezYounan/easy_date_timeline/master/screenshots/locale_support_example.jpg"/>
</p>

```dart
    EasyDateTimeLine(
      initialDate: DateTime.now(),
      onDateChange: (selectedDate) {
        //`selectedDate` the new date selected.
      },
      activeColor: const Color(0xffB04759),
      locale: "ar",
    );
```

## Landscape view

With `easy_date_timeline`, you can display dates and timelines in landscape view just set
`landScapeMode` to `true` in `dayProps`.

<p>
 <img src="https://raw.githubusercontent.com/FadyFayezYounan/easy_date_timeline/master/screenshots/landscape_view_example_2.jpg"/>
</p>

```dart
    EasyDateTimeLine(
      initialDate: DateTime.now(),
      onDateChange: (selectedDate) {
        //`selectedDate` the new date selected.
      },
      activeColor: const Color(0xff116A7B),
      dayProps: const EasyDayProps(
        landScapeMode: true,
        activeDayStyle: DayStyle(
          borderRadius: 48.0,
        ),
        dayStructure: DayStructure.dayStrDayNum,
      ),
      headerProps: const EasyHeaderProps(
        dateFormatter: DateFormatter.fullDateDMonthAsStrY(),
      ),
    )
```

## Change header appearance

In the `headerProps` change the `monthPickerType` to:

- `MonthPickerType.switcher` : show the month and you can change month by clicking the arrow buttons.
- `MonthPickerType.dropDown` : show the month and you can change month from a dropdown menu.
- also in the `headerProps` change the `dateFormatter` to:
- `DateFormatter.dayOnly()` : Formats the date with only the day of the week for example "Monday".
- `DateFormatter.monthOnly()` : Formats the date with only the month for example "January".
- `DateFormatter.fullDateDMY()` : Formats the date as "day/month/year" (e.g., "01/01/2022"), You can also specify a custom separator to use between the day, month, and year. default separator is "/".
- `DateFormatter.fullDateMDY()` : Formats the date as "month/day/year" (e.g., "01/25/2022"), You can also specify a custom separator to use between the day, month, and year. default separator is "/".
- `DateFormatter.fullDateDayAsStrMY()` : Formats the date as "day month, year" (e.g., "Monday 12, 2022"), You can also specify a custom separator. default separator is ", ".
- `DateFormatter.fullDateDMonthAsStrY()` : Formats the date as "day month year" (e.g., "1 January, 2022"), You can also specify a custom separator. default separator is ", ".
- `DateFormatter.fullDateMonthAsStrDY()` : Formats the date as "month day, year" (e.g., "January 1, 2022"), You can also specify a custom separator. default separator is ", ".
- `DateFormatter.custom()` : Formats the date using a custom formatter.

<p>
 <img src="https://raw.githubusercontent.com/FadyFayezYounan/easy_date_timeline/master/screenshots/change_header_appearance_example.jpg"/>
</p>

```dart
    EasyDateTimeLine(
      initialDate: DateTime.now(),
      onDateChange: (selectedDate) {
        //`selectedDate` the new date selected.
      },
      activeColor: const Color(0xff37306B),
      headerProps: const EasyHeaderProps(
        monthPickerType: MonthPickerType.switcher,
        dateFormatter: DateFormatter.fullDateDayAsStrMY(),
      ),
      dayProps: const EasyDayProps(
        activeDayStyle: DayStyle(
          borderRadius: 32.0,
        ),
        inactiveDayStyle: DayStyle(
          borderRadius: 32.0,
        ),
      ),
      timeLineProps: const EasyTimeLineProps(
        hPadding: 16.0, // padding from left and right
        separatorPadding: 16.0, // padding between days
      ),
    )
```

<a id="itemBuilder-example"></a>

## Customize day appearance

> **IMPORTANT NOTE:**
>
> When utilizing the `itemBuilder`, it is essential to provide the width of each day for the date timeline widget.

- For example:

```dart
  dayProps: const EasyDayProps(
   // You must specify the width in this case.
   width: 124.0,
  ),
```

You can use the `itemBuilder` to customize the appearance of the day widget.
The `itemBuilder` provides the following:

- `BuildContext context`.
- `String dayNumber` : the day number ex: "11".
- `String dayName` : the day name ex: "Sunday".
- `String monthName` : the month name ex: "June".
- `DateTime fullDate` : the full date of the day for fully customization.
- `bool isSelected` : whether the day is selected or not.

<p>
 <img src="https://raw.githubusercontent.com/FadyFayezYounan/easy_date_timeline/master/screenshots/customize_day_appearance_example.jpg"/>
</p>

```dart
    EasyDateTimeLine(
      initialDate: DateTime.now(),
      onDateChange: (selectedDate) {
        //`selectedDate` the new date selected.
      },
      dayProps: const EasyDayProps(
        height: 56.0,
        // You must specify the width in this case.
        width: 124.0,
      ),
      headerProps: const EasyHeaderProps(
        dateFormatter: DateFormatter.fullDateMonthAsStrDY(),
      ),
      itemBuilder: (context, date, isSelected, onTap) {
        return InkWell(
          // You can use `InkResponse` to make your widget clickable.
          // The `onTap` callback responsible for triggering the `onDateChange`
          // callback.
          onTap: onTap,
          borderRadius: BorderRadius.circular(16.0),
          child: Container(
            //the same width that provided previously.
            width: 124.0,
            padding: const EdgeInsets.symmetric(horizontal: 8.0),
            decoration: BoxDecoration(
              color: isSelected ? const Color(0xffFF6D60) : null,
              borderRadius: BorderRadius.circular(16.0),
            ),
            child: Row(
              mainAxisAlignment: MainAxisAlignment.center,
              children: [
                Text(
                  EasyDateFormatter.shortMonthName(date, "en_US"),
                  style: TextStyle(
                    fontSize: 12,
                    color: isSelected ? Colors.white : const Color(0xff6D5D6E),
                  ),
                ),
                const SizedBox(
                  width: 8.0,
                ),
                Text(
                  date.day.toString(),
                  style: TextStyle(
                    fontSize: 20,
                    fontWeight: FontWeight.bold,
                    color: isSelected ? Colors.white : const Color(0xff393646),
                  ),
                ),
                const SizedBox(
                  width: 8.0,
                ),
                Text(
                  EasyDateFormatter.shortDayName(date, "en_US"),
                  style: TextStyle(
                    fontSize: 12,
                    color: isSelected ? Colors.white : const Color(0xff6D5D6E),
                  ),
                ),
              ],
            ),
          ),
        );
      },
    )
```

##### Constructor:

```dart
  EasyDateTimeLine({
    super.key,
    required this.initialDate,
    this.disabledDates,
    this.headerProps = const EasyHeaderProps(),
    this.timeLineProps = const EasyTimeLineProps(),
    this.dayProps = const EasyDayProps(),
    this.onDateChange,
    this.itemBuilder,
    this.activeColor,
    this.locale = "en_US",
  });
```

```dart
  EasyInfiniteDateTimeLine({
    super.key,
    this.disabledDates,
    this.timeLineProps = const EasyTimeLineProps(),
    this.dayProps = const EasyDayProps(),
    this.onDateChange,
    this.itemBuilder,
    this.activeColor,
    this.locale = "en_US",
    required this.firstDate,
    required this.focusDate,
    required this.lastDate,
    this.controller,
    this.showTimelineHeader = true,
    this.headerBuilder,
  });
```

## Additional information

- **Contributing**: Contributions to the Easy Date Timeline package are welcome! [GitHub repository](https://github.com/FadyFayezYounan/easy_date_timeline/pulls).
- **Filing issues**: If you encounter any issues with the Easy Date Timeline package, please file an issue on the [GitHub repository](https://github.com/FadyFayezYounan/easy_date_timeline/issues).
- **Support**: If you have any questions or need help using the Easy Date Timeline package, please feel free to reach out to the package authors on [GitHub](https://github.com/FadyFayezYounan).

We hope you find the Easy Date Timeline package helpful!
