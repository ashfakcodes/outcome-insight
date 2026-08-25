# Technical Overview

## Application

**Outcome Insight** is an Android application for Bangladeshi students to access examination results through supported government-operated web portals and SMS workflows.

Package name:

```text
com.xiluxstudio.oi
```

## Platform

- Android
- Minimum API: 21
- Target API: 34
- Java
- XML Views

## Dependencies

Known project dependencies include:

- OkHttp
- Material Components

The final source repository should document the exact dependency versions from the Gradle configuration rather than guessing them.

## Result portal integration

There is no public API for the supported result systems, so the application relies on the corresponding government-operated web portals.

The application does not claim to replace those portals. Instead, it provides a more focused Android interface for accessing them.

## Web-page customization

Some result websites contain navigation, promotional, or other interface elements that are not useful while viewing a result.

Outcome Insight uses JavaScript injection in supported web content to remove selected unnecessary elements. This reduces visual clutter while preserving the important result information.

This behavior should remain scoped to supported pages and selectors. Website redesigns can require maintenance because DOM structures and element identifiers may change.

## Multiple result portals

Government result portals may experience heavy traffic during result publication.

Outcome Insight supports two websites for the relevant result workflow, providing an alternative when one portal is experiencing availability or traffic problems.

## SMS workflow

The SMS workflow is intentionally user-controlled.

1. The user selects the examination type.
2. The user selects the board.
3. The user selects the examination year.
4. Outcome Insight constructs the required SMS text.
5. Android's native messaging application is opened with the generated message.
6. The user reviews and manually sends the SMS.
7. The application does not automatically read or parse the response.

This approach avoids requiring the application to automatically send or read SMS messages.

## PDF export

The application can convert the displayed result page into a PDF so the user can retain a copy of the result.

## Privacy model

The application is described as not collecting or storing personal student data such as roll or registration numbers.

Known permission requirement:

```text
android.permission.INTERNET
```

The application contains advertisements.

No Firebase Analytics or Crashlytics integration is currently documented.
