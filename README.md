# Time
Time and Clock app built as a standalone app or to integrate with our MODE Handyman app for employee management.

Time

Android Clock, Employee Timekeeping, and Job Tracking Application

Developed by Maclean Of Duart Enterprises Corp

Version: 1.0.6
Version Code: 7
Platform: Android
License: GNU General Public License v3.0 (GPL-3.0)

Overview

Time is a native Android clock and employee timekeeping application developed by Maclean Of Duart Enterprises Corp.

The application combines a customizable clock, alarms, countdown timer, employee timecards, job tracking, work-hour calculations, and administrative controls into one locally managed system.

Time is designed for employees, subcontractors, independent contractors, small businesses, and individuals who need a straightforward way to manage their working hours.

It also integrates with MODE Handyman, allowing businesses to distribute employee and job configurations and import completed timecards for payroll processing.

Time emphasizes:

- Local data ownership.
- Offline-first operation.
- Employee and job management.
- Accurate work-hour recording.
- Simple clock-in and clock-out procedures.
- Administrative access controls.
- Customizable clock and alarm functions.
- CSV and JSON interoperability.
- Independence from mandatory cloud services.

Main Features

1. Clock and Time Display

Time includes a customizable clock interface.

Features include:

- Local time display.
- Searchable world time zones.
- Analog clock.
- Digital clock.
- Combined analog and digital display.
- 12-hour and 24-hour formatting.
- Optional seconds display.
- Device time-zone synchronization.

Clock preferences are configurable through Settings.

2. Employee and Worker Profiles

Access through:

Profiles → Workers

Features include:

- Create employee profiles.
- Edit employee information.
- Delete employee profiles.
- Store employee names.
- Store optional employee identification numbers.
- Associate workers with MODE Handyman business profile identifiers.
- Maintain custom employee information.
- Import employee profiles from CSV.
- Export employee profiles to CSV.
- Import employee setup JSON files.
- Select the active worker for timekeeping.

Worker profiles can contain custom fields such as contact information and business-specific details.

When administrative controls are enabled, profile modifications require authorization.

Deleting an employee permanently removes their associated shifts, breaks, and attached files after confirmation.

3. Job and Worksite Management

Access through:

Profiles → Jobs

Features include:

- Create jobs.
- Edit existing jobs.
- Delete jobs.
- Archive and restore jobs.
- Assign job names.
- Configure job codes.
- Store job-site addresses.
- Add custom job information.
- Configure job-specific pay multipliers.
- Select jobs when clocking in.
- Import job profiles using CSV.
- Export active job profiles to CSV.

Jobs can include custom fields such as customer information, project descriptions, or project leads.

Previously recorded timecards preserve their job details when a job is edited, archived, or deleted.

4. Jobsite Navigation

Time supports navigation to saved job-site destinations.

Supported navigation options include:

- OsmAnd.
- Google Maps.
- OpenStreetMap.
- Other compatible Android mapping applications.

Job-site addresses can be configured manually or imported through employee setup files.

OsmAnd street-address navigation may require an online OpenStreetMap lookup.

5. Employee Timecards

Access through:

Timecard

Time provides employee time tracking with selectable workers and jobs.

Features include:

- Select an employee.
- Select an active job.
- Clock in.
- Clock out.
- Start unpaid breaks.
- End unpaid breaks.
- Record optional shift notes.
- Track completed working time.
- Maintain active shifts across application restarts.
- View recorded shifts.
- Review total paid hours.

Each employee can have one open shift.

Timecards can also be recorded without assigning a specific job.

Job names, codes, and applicable pay multipliers are captured when a shift begins.

6. Manual Time Entries and Corrections

Time supports manual time entry for missed punches and corrections.

Features include:

- Add manual shifts.
- Edit completed shifts.
- Correct clock-in times.
- Correct clock-out times.
- Edit unpaid break durations.
- Update shift notes.
- Record overnight shifts.
- Recalculate paid working hours.
- Delete individual completed shifts.
- Delete completed timecards by pay period.

Administrative authorization is required for corrections and deletions when admin controls are enabled.

Deleting a timecard removes completed shifts for the selected worker and displayed date range without deleting other workers' records or active shifts.

Previously exported CSV files remain independent copies.

7. Pay Periods and Working-Hour Calculations

Time provides selectable date ranges for reviewing work records.

Features include:

- Select a starting date.
- Select an ending date.
- Review completed shifts.
- Calculate paid working time.
- Exclude unpaid breaks.
- Preserve exact paid seconds.
- Include applicable job multipliers in exported records.
- Calculate totals for the selected period.

The selected From and Through dates are inclusive.

Overnight shifts are supported.

Shifts exceeding 24 hours are divided into appropriate export rows.

Time also preserves actual paid durations when clock changes or daylight saving time transitions affect recorded shifts.

8. Timecard CSV Export

Completed timecards can be exported as UTF-8 CSV files.

Access through:

Timecard → Export timecard CSV

Exported information includes:

- Employee identification.
- Business profile identification where available.
- Work dates.
- Clock-in and clock-out times.
- Unpaid break minutes.
- Exact paid seconds.
- Pay multipliers.
- Shift notes.
- Job names and codes in the notes.
- Pay-period dates.

Users select the destination for the exported file using Android's document picker.

These files can be imported into compatible business-management applications, including MODE Handyman.

9. MODE Handyman Integration

Time is designed to work alongside MODE Handyman's employee, subcontractor, and payroll management features.

MODE Handyman can export employee setup JSON files containing supported worker and job information.

Time can import these files through:

Settings → Import employee setup JSON

Supported setup information includes:

- Employee names.
- Employee identification numbers.
- Business profile identifiers.
- Employee contact information.
- Assigned jobs.
- Job codes.
- Job-site addresses.
- Custom profile fields.
- Job pay multipliers.
- Optional application settings.
- Employee attachments.

The importer also accepts supported MODE payroll worker objects.

Payroll rates, taxes, and paystub processing remain managed in MODE Handyman.

After importing a valid single-employee setup file, Time selects that employee on the Timecard screen.

10. Intelligent Profile Import and Duplicate Handling

Time supports updating existing employee and job records through imported setup files.

Features include:

- Match employees by MODE identifiers.
- Match employees by normalized names.
- Ignore capitalization differences.
- Ignore unnecessary spacing differences.
- Update existing employee information.
- Consolidate compatible duplicate employee records.
- Preserve existing shifts.
- Preserve employee attachments.
- Maintain separation between distinct known businesses.
- Match jobs by code.
- Match jobs by name when no code is available.
- Preserve existing time records during profile updates.

When an imported MODE employee matches an existing manual employee, Time can associate the existing employee with the supplied MODE identifiers.

Compatible duplicate records can be consolidated while retaining their timecards and attachments.

If duplicate profiles both have active shifts, one must be clocked out before consolidation.

Invalid imports are rejected without partially applying their changes.

11. Employee Setup JSON

Time supports configurable employee setup files using the format:

"time.setup.v1"

Supported JSON sections include:

- "settings"
- "employees"
- "worker"
- "jobs"
- "addresses"
- "fields"
- "files"

Setup files can configure:

- Application theme.
- Clock display style.
- Hour format.
- Seconds display.
- Employee profiles.
- Job profiles.
- Job-site addresses.
- Custom information.
- Employee attachments.

Files must use UTF-8 JSON.

The maximum supported setup file size is 16 MiB, including Base64-encoded attachments.

Attachments are stored locally and can be accessed through the employee profile interface.

12. Administrative Controls

Access through:

Settings → Admin panel

Time includes optional administrative controls for protecting employee and job information.

Features include:

- Enable or disable admin controls.
- Configure a 6–12 digit administrator PIN.
- Restrict employee profile modifications.
- Restrict job profile modifications.
- Protect CSV imports.
- Protect job pay multipliers.
- Restrict timecard corrections.
- Restrict timecard deletion.
- Protect job archiving and restoration.
- Lock the admin panel when leaving it.
- Require reauthorization when appropriate.

Ordinary employees can continue viewing profiles, selecting workers and jobs, and recording working time.

Administrative controls are local to the device.

Clearing application storage or uninstalling Time removes locally stored records and the PIN.

13. Authorized Employee Setup Imports

Time supports importing employee setup files without repeatedly requesting the administrator PIN when the file contains valid authorization.

Three supported approaches are available:

Standard PIN Authorization

An administrator can include the receiving device's existing admin PIN in a setup JSON file using the "admin_password" field.

A valid PIN authorizes the import.

Authorized JSON Creator

Access through:

Settings → Admin panel → Add admin PIN to setup JSON

This allows an administrator to select a setup file, supply the receiving device's existing PIN, and save an authorized copy.

Cryptographically Signed Setup Files

Time supports trusted-sender signatures for setup imports without distributing the receiving device's administrator PIN.

The administrator can:

- Display the device's public sender key.
- Enroll a trusted sender key on the receiving device.
- Sign employee setup files.
- Distribute signed setup files.
- Revoke a trusted sender.

Signed setup files use ECDSA P-256 with SHA-256 and the format:

"time.signed.v1"

The receiving device verifies the signature before applying the imported configuration.

Modified files or files signed by an untrusted sender fail verification.

Security note: A setup file containing an administrator PIN exposes that PIN to anyone who can read the file. Trusted signatures are preferable when the administrator does not want to distribute the PIN.

14. Worker and Job CSV Management

Time supports CSV-based profile management.

Worker CSV files support:

- "employee_name"
- "employee_id"
- "business_profile_id"
- Additional custom columns.

Job CSV files support:

- "job_name"
- "job_code"
- "multiplier"
- Additional custom columns.

Supported delimiters include:

- Commas.
- Semicolons.
- Tabs.

Quoted fields support embedded delimiters and newlines.

Imported records update matching profiles according to the supported identification rules.

Omitted custom fields retain their previous values.

Rejected import batches leave existing profiles unchanged.

15. Alarms

Time includes a configurable alarm system.

Features include:

- Create alarms.
- Edit alarms.
- Delete alarms.
- Enable or disable individual alarms.
- Configure alarm labels.
- Select alarm times.
- Configure one-time alarms.
- Configure repeating alarms.
- Select individual weekdays.
- Use sound-only alerts.
- Use vibration-only alerts.
- Combine sound and vibration.
- Preview alerts before saving.

Each alarm has its own on/off switch.

Disabling an alarm preserves its settings.

One-time alarms automatically switch off after ringing and can be re-enabled.

16. Custom Alarm Sounds

Time supports configurable alarm sounds.

Options include:

- Built-in Time chime.
- Android-installed ringtones.
- Imported audio files.

Imported audio files are copied into local application storage.

This allows the sound to remain available even when the original selected file is moved.

The built-in chime provides a fallback when a selected system tone becomes unavailable.

Alarm sound playback uses Android's alarm volume.

17. Custom Alarm Vibrations

Time includes configurable vibration patterns.

Features include:

- Built-in vibration presets.
- Custom vibration sequences.
- Import vibration patterns from text files.
- Import vibration patterns from CSV files.
- Preview vibration patterns.

Custom sequences use alternating pause and vibration durations in milliseconds.

Example:

"0,300,200,600"

18. Countdown Timer

Time includes a countdown timer with:

- Custom countdown durations.
- Start.
- Pause.
- Resume.
- Reset.
- Completion notifications.

Active timers are restored after supported device restarts.

Android notification and exact-alarm permissions may be required for reliable background operation.

19. Settings and Appearance

Access Settings using the gear icon in the upper-right corner.

Available settings include:

- Automatic theme.
- Light theme.
- Dark theme.
- Analog clock display.
- Digital clock display.
- Combined clock display.
- 12-hour formatting.
- 24-hour formatting.
- Optional seconds display.
- Administrative controls.
- Employee setup JSON import.
- Authorized setup file management.

The application also includes configurable local and world clock displays.

20. Notifications and Background Operation

Time uses Android's native notification and scheduling mechanisms.

Features include:

- Alarm notifications.
- Timer completion notifications.
- Scheduled alarm restoration.
- Active timer restoration.
- Device restart handling.
- Time-zone change handling.
- Clock-change handling.
- Application replacement handling.

Android 13 and later may require notification permission.

Exact-alarm access may also be required, depending on the Android version and device configuration.

Users should allow the requested permissions for reliable alarms and timers.

Privacy and Data Ownership

Time is designed to operate without mandatory accounts or cloud synchronization.

The application uses:

- Local application storage.
- A local database.
- Android document selection.
- Android file sharing.
- Local employee and job records.
- Local timekeeping records.
- Android Keystore for signing-key protection.

Clock and timecard functions operate offline.

Internet access is declared for supported operations such as online address lookup.

The application does not require broad storage access.

Android automatic application backup is disabled in the manifest.

Users should retain independent copies of important exported records.

Technical Information

Property| Value
Application| Time
Version| 1.0.6
Version code| 7
Android package| com.macleanofduartenterprises.time
Programming language| Kotlin
Platform| Native Android
Minimum Android| Android 8.0 (API 26)
Target Android API| 35
Compile SDK| 35
Android Gradle Plugin| 8.10.1
Kotlin plugin| 1.9.25
JDK| 17 or 21
Storage| Local application database and files
Architecture| Offline-first
Employee import| JSON / CSV
Timecard export| UTF-8 CSV
License| GPL-3.0
Development environment| Android Studio / Gradle

Source Architecture

Time is a focused adaptation of Simple Time Tracker 1.61 by Razeeman.

The retained time-tracking core includes:

- Record.
- RunningRecord.
- RecordBase.
- MultitaskRecord.
- Range.
- RangeMapper.
- Common domain extensions.

The MODE-specific implementation provides:

- Native clock screens.
- Employee profiles.
- Job profiles.
- Administrative controls.
- Local application database.
- Employee setup imports.
- MODE Handyman interoperability.
- Custom alarm functions.
- Countdown timer.
- CSV export and import.
- Local signed-file authorization.

Original upstream project:

https://github.com/Razeeman/Android-SimpleTimeTracker

The included GPLv3 license applies to this derivative application.

What's New in Version 1.0.6

Version 1.0.6 builds on the employee, timecard, clock, and administrative functionality introduced in previous releases.

The current source includes:

- Employee and job profile deletion.
- Duplicate employee consolidation during setup imports.
- Admin PIN authorization for employee setup files.
- Trusted-sender signed JSON imports.
- Individual alarm enable/disable switches.
- Custom alarm sounds and vibration patterns.
- Configurable clock appearance.
- Light, dark, and automatic themes.
- Employee timecard editing and deletion.
- CSV timecard exports for MODE Handyman.
- Improved profile and setup import validation.
- Local notification and alarm restoration support.

Building the Application

Requirements:

- JDK 17 or 21.
- Android SDK Platform 35.
- Android Studio or a compatible Gradle build environment.

Build the release APK:

./gradlew assembleRelease

The resulting release APK must be signed using the developer's Android release keystore.

Signing credentials should be maintained outside the source repository.

Testing and Verification

The source project includes verification utilities covering:

- Employee setup imports.
- Profile matching and updates.
- Device behavior.
- Alarm scheduling.
- Alert configuration.
- Payroll data interoperability.
- Application updates.

Before distributing a production release, verify:

- Employee and job creation.
- Profile editing and deletion.
- Clock-in and clock-out.
- Break tracking.
- Manual time entries.
- Timecard corrections.
- CSV exports.
- MODE Handyman imports.
- Admin PIN authorization.
- Signed setup file verification.
- Alarm notifications.
- Background timer operation.
- Application upgrades.
- Local data preservation.

Source inspection and included verification code do not substitute for complete physical-device testing.

License

Time is distributed under the GNU General Public License version 3.0 (GPL-3.0).

License information:

https://www.gnu.org/licenses/gpl-3.0.html

The application incorporates components derived from Simple Time Tracker, with the applicable GPLv3 license retained.

Developer

Maclean Of Duart Enterprises Corp

Website:

https://macleanofduartenterprises.com

Project Identity

Time — Clock and Employee Timekeeping

A native Android application combining customizable clock functions, alarms, timers, employee timecards, job management, administrative controls, and MODE Handyman integration.

Designed to provide practical, locally managed timekeeping without requiring a proprietary cloud account.

Version: 1.0.6
Platform: Android
Development: Native Kotlin
Data Architecture: Local-first
License: GPL-3.0
