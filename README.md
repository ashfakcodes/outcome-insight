# Outcome Insight

> A modern Android companion for accessing Bangladesh's Board and National University examination results.

**Outcome Insight** is an Android application designed to make checking examination results easier for Bangladeshi students. It provides access to government-operated result portals, supports SMS-based result requests, and lets users save result pages as PDF files.

The app was independently designed and developed from the ground up.

## Highlights

- 📱 Android application built with Java and XML Views
- 🎓 Board examination result access
- 🏫 National University result access
- 📩 SMS result request formatting
- 📄 Save result pages as PDF
- 🌐 Support for Bengali and English
- 📴 Useful offline functionality
- 🧹 Cleaner result-page experience by removing distracting website elements
- 🔁 Alternative result websites to help when government portals experience heavy traffic
- 📢 Ad-supported
- 👤 No personal data collection or storage of roll/registration numbers

## Supported examinations

Outcome Insight supports result systems for:

- SSC
- HSC
- JSC
- Equivalent examinations
- National University Honours
- National University Degree
- National University Masters
- National University Professional examinations

## How it works

### Web-based results

Outcome Insight relies on government-operated examination result websites because there is no public API available for the supported result systems.

The app presents the relevant result portal to the student and lets the student enter the required examination information, such as their roll/registration details.

Some government result portals can become difficult to access during result publication because of heavy traffic. Outcome Insight therefore provides two alternative supported result sites where applicable.

The app also improves the viewing experience by injecting JavaScript into the displayed result pages to remove unnecessary or distracting interface elements, keeping the student's attention on the result itself.

### SMS results

The app helps students request results through the government's SMS-based result system.

The student selects the relevant:

- Examination type
- Board
- Examination year

Outcome Insight then generates the required SMS format. The formatted message is handed to Android's native messaging application, where the student manually sends it.

The app does **not** automatically send or read SMS messages and does not parse the SMS response.

## PDF export

Result pages can be converted and saved as PDF, giving students a convenient copy of their result information for later reference.

## Technology

| Component | Technology |
|---|---|
| Language | Java |
| UI | XML Views |
| Minimum Android version | API 21 |
| Target Android version | API 34 |
| Networking | OkHttp |
| UI components | Material |
| Web interaction | Android WebView / web content |
| Web customization | JavaScript injection |

## Design

Outcome Insight was designed with a clean, modern, minimal visual style.

The UI and UX were designed independently for the application, with the goal of keeping the result-checking process straightforward rather than overwhelming students with unnecessary controls.

## Privacy

Outcome Insight does not collect or store personal student information such as roll numbers or registration numbers.

The application uses Internet access to load supported result portals and contains advertisements.

Privacy policy:

[Outcome Insight Privacy Policy](https://xiluxstudio.great-site.net/oi/privacy-policy)

## Project history

| Milestone | Date |
|---|---|
| Development started | December 15, 2023 |
| First published | February 5, 2024 |
| Distribution | Amazon Appstore, Uptodown |
| Downloads / users | 1K+ |
| Current status | Maintained occasionally |

## Engineering highlights

One of the more interesting implementation challenges was dealing with government result portals that contain interface elements which can distract from the actual result.

Outcome Insight uses JavaScript injection to selectively remove unnecessary elements from supported pages while leaving the relevant result content accessible to the student.

Another practical challenge is handling result-day traffic. Government result systems can experience significant load when large numbers of students check results simultaneously. Outcome Insight therefore supports two result websites where applicable, giving students an alternative route when one portal is unavailable or overloaded.



## Project structure

This repository is intended to document and showcase Outcome Insight as a portfolio project.


Documentation:

```text
docs/
├── technical-overview.md
└── portfolio-notes.md
```

Visual assets:

```text
screenshots/
```

## Development notes

Outcome Insight was developed independently, including:

- UI design
- UX decisions
- Android implementation
- Application logic
- Result portal integration
- SMS formatting workflow
- PDF export workflow
- Web-page customization
- Navigation and application behavior

No claim is made here about a formal architecture pattern because the project documentation does not currently specify one.

## Author

**Ashfak Sourav**

Independent Android developer and UI/UX designer.

## License

See [`LICENSE`](LICENSE).

---

### Disclaimer

Outcome Insight is an independent application for accessing examination result information through supported result systems. It is not affiliated with, endorsed by, or operated by any Bangladeshi education board, the National University, or other government organization unless explicitly stated by those organizations.

Users should verify important academic information through the relevant official examination authority.
