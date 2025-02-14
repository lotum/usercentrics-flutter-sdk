[Release Notes](https://docs.usercentrics.com/cmp_in_app_sdk/latest/about/history/)

### 2.11.2 - January 10, 2024

## Improvements

* Rework of session restore checks to prevent empty/bogus Controller ID

## Android Bug Fixes

* Controller ID card replaced at the bottom when using Google Additional Consent
* Language selection menu will respect programmatic customization parameters
* Warning for Chartboost SDK when R8 is enabled
* Minor UI glitch where tab names were truncated when displaying the second layer in landscape mode

## iOS Bug Fixes

* Prevent fatal exceptions for a known iOS issue, more details [here](https://developer.apple.com/forums/thread/115405)

## Other Fixes

* Solved for Webview continuity previously not restoring consents to Google Additional Technology Providers
* Solves the problem where the option 'Show non-IAB purposes only for EU users' incorrectly impacts users from specific regions
* Application of consents when configuring the CMP to 'Do Not Display' with Geolocation Rules

### 2.11.1 - January 05, 2024

## Resolved Issues

* Google Additional Consent Mode V2 - models were not exported and publicly available :cry:

### 2.11.0 - December 22, 2023

## Features

* Google Consent Mode V2 Support - Seamlessly integrate with the latest Google Consent Mode, ensuring enhanced privacy compliance and meeting Google requirements.
* Google Additional Consent Mode V2 - Integrate with the latest Google Additional Consent, allowing you to collect and signal additional consent for ad tech providers not covered by the IAB TCF V2.2.
* Display Number of Vendors for Each Purpose on TCF - Easily view the number of vendors associated with each purpose in the Transparency and Consent Framework.
* Chartboost SDK in Consent Mediation - Optimize revenue by effortlessly managing the Chartboost SDK within Usercentrics Consent Mediation.

## Improvements

* TCFUserDecisions API update - All properties have been changed from variables to constants. The adTechProviders field has been added which represent consents for Google Additional Consent Mode. On iOS this is a required argument, so if this is irrelevant for your configuration, just set an empty list, when needed. 
* Location is only cached by the SDK for offline mode.

## Android Resolved Issues

* Avoid fetching any image resource after the banner has been closed.

## iOS Resolved Issues

* Prevent Long Privacy Legal Links from Being Truncated.
* Enable Scaled Fonts resources when using Custom UI.

## Other Resolved Issues

* Third-Party Vendors Count misalignment in some configurations.
* Fix the bug causing the banner to reappear for users outside the European Union, despite configurations being specifically set to enforce GDPR compliance exclusively for EU users.
* Update Link to Report Issues on Zendesk.

### 2.10.0 - November 16, 2023

## Improvements

* Accessibility: Various issues have been addressed to enhance accessibility. 
  * Resolved banner compatibility issues with iOS VoiceOver.
  * Resolved banner compatibility issues with Android TalkBack.
  * Adjusted font sizes to comply with Accessibility requirements on both iOS and Android.

* Added Ukrainian support language for TCF.

## Resolved Issues

* Fixed the issue of not disclosing the setting "showCloseButton" has been addressed, preventing errors on Android. 
* Fixed the crash on Android when passing an invalid controller id to restore the user session. 
* Fixed The issue of the remote variant configuration not being used in first layer on Unity. 

### 2.9.0 - October 6, 2023

## Features

* :rocket: **Full TCF 2.2 Support**: As the industry shifts to TCF 2.2 (deadline: November 20, 2024), we are pleased to announce that SDK Version 2.9.0 now offers comprehensive support for this new industry standard.
* :warning: **Important Note**: Please be aware that this version is incompatible with TCF 2.0. Before upgrading to V 2.9.0, ensure a smooth transition to TCF 2.2 following the  guidelines:

[How to migrate from TCF v2.0 to TCF v2.2](https://usercentrics.atlassian.net/wiki/spaces/SKB/pages/2668789801/How+to+migrate+from+TCF+v2.0+to+TCF+v2.2#\uD83D\uDCD8-Migration-instructions-for-TCF-v2.2)

## Key Changes and Enhancements:

* Updated Global Vendor List: We've transitioned to Global Vendor List v3 to align with industry standards.
* Legitimate Interest: To enhance transparency and privacy, purposes 3 to 6 have been removed, and purpose 11 has been introduced.
* Improved User Interface: We've made enhancements to the banner's second layer for a better user experience.
* Vendor Count Display: Users can now easily see the total count of IAB and non-IAB vendors.
* New Resurface Requirements: We've implemented new resurfacing requirements to keep your CMP compliant with the latest standards.

### 2.8.4 - September 27, 2023

## Improvements

* TCF performance is now improved for settings with a huge amount of vendors

## Resolved Issues

* UI small issues
* Solved general issues


### 2.8.3 - September 4, 2023
 
## Resolved Issues

* UI small issues on iOS (labels being cut, when they have long values)
* Fixed Deprecated DPS being shown
* Solved general issues

### 2.8.2 - July 12, 2023

## Features

* [Unity] New GetCmpData API, check out the documentation [here](https://docs.usercentrics.com/cmp_in_app_sdk/latest/unity/core-api/#get-cmp-data) :tada:
* [Flutter and RN] Track API is live, check out the documentation [here](https://docs.usercentrics.com/cmp_in_app_sdk/latest/api/usercentrics-core/#track) :tada:

## Improvements

* Enabled support for Hide Data Processing Services
* Added a "default" label into consent history entries, when it was given implicitly

## Resolved Issues

* Consent mediation improvements
* Solved general issues

### 2.8.1 - June 9, 2023

## Improvements

* `onConsentUpdated` event is not triggered after initialization
* Banner reshow logic

## Resolved Issues

* Boolean values sent via consent mediation to Adjust
*  Apple TV labels being cut off
*  Android TV issue when showing TCF on 2nd layer
*  Solved general issues

### 2.8.0 - May 8, 2023

## Features

* Support US Frameworks

## Improvements

* Remove deprecated method (showFirstLayer(layout: UsercetricsLayout))

## Resolved Issues

* Mediation issues
* Solved general issues

### 2.7.16

## Features

* Supporting Limited Fields in Service Descriptions.

## Improvements

* Improvements in accessibility.
* Custom UI objects are getting the latest values.

## Resolved Issues

* Solve general issues

### 2.7.15

## Resolved Issues

* Solve general issues.

* Solve issue when switches were showing the wrong value on iOS when pressing too many times repeatedly.

* Solve issue when toggles were showing on second layer even though they were disabled.

* Solve issue where the first time the app was initialized using the method getTCString, the TCString comes out empty.

* Fixed issue where DPSs accepted by default did not appear as accepted when opening second layer.

### 2.7.13

## Features

* Enabling PUR customisation properties

## Improvements

* Improvements to stability and exception handling to solve edge cases.

## Resolved Issues

* Solve issue with third party SDKs being included in POM file.
* UI improvements to CCPA Banner solution

### 2.7.12

## Improvements

* Several improvements on Consent Mediation 
    * Add support for Adjust and Crashlytics.
    * Add support for Custom DPSs.

## Resolved Issues

* Stability improvements and bug fixes.

### 2.7.10

## Improvements

* [TCF] Performance improvement.

## Features

* Stability improvements and bug fixes.

### 2.7.9

## Features

* Add a property to disable the system back button in the first layer

### 2.7.8

## Features

* First Layer Banner has met accessibility requirements :tada:
* Remotely configure your banner layout option of your banner. This feature is only for "App Advanced" Configurations. Please contact your CSM if you would like to get access to this feature.

## Resolved Issues

* Solve CCPA issue with toggle initial value.
* Stability improvements and bug fixes

### 2.7.6

## Improvements

* Major improvements to main thread use.

## Resolved Issues

* [Android] Resolve NPE crash happening in edge cases.
* Stability improvements.

### 2.7.5

## Improvements

* Major improvements to main thread use.

## Resolved Issues

* [Android] Resolve NPE crash happening in edge cases.
* Stability improvements.

# 2.7.4

## Features
 
* **[A/B Testing]** With this release, you will now be able to create your own A/B Testing when showing the banner to your users. Check our [exclusive page](https://docs.usercentrics.com/cmp_in_app_sdk/latest/features/ab-testing) on how to achieve this.

## Improvements

* General bug fixes.
* [iOS] Support dynamic colors.

# 2.7.3

## Improvements

* General bug fixes.
* Huge performance improvement.

# 2.7.2

## Features

* **[Compliance]** You may now enable a close button in the First Layer, to "Continue without accepting".

## Improvements

* Improve legal link customization via our Programmatic API.
* Upgrade Error logs to help you debug the SDK's behaviour.

## Resolved Issues

* [TCF 2.0] Solve issue where shouldCollectConsent was always true.

# 2.7.1

## Features

* **[Restore User Session][TCF]** With this release, you will now be able to restore user sessions when using a TCF configuration. This feature however, needs to be enabled and approved. Please contact your Customer Success Manager for more information.

## Improvements

* API upgrades to improve performance and storage space usage.
* **[TCF]** Updates to TCF logic, for custom use cases.

## Resolved Issues

* **[iOS][Dark Mode]** Solve issue where SDK was overwritting theme to always be "light".
* Improvements to solve "NullPointerException" and unknown origin crashes.

# 2.7.0

## Features

- **[Dark Mode][Customization API]** Support Dark Mode and create advanced banner customizations with our updated [Customization API](https://docs.usercentrics.com/cmp_in_app_sdk/latest/collect_consent/usercentrics-ui/#programmatic-customization). :first_quarter_moon:
- **[Beta][Consent Mediation]** Automatically apply consent to 3rd party SDKs with our [Consent Mediation](https://docs.usercentrics.com/cmp_in_app_sdk/latest/apply_consent/consent-mediation) feature. :partying_face:
- UI improvements to history section.
- Added additional customization options for TCF 2.0 banner.

## Resolved Issues

- Solved stability issues.

# 2.6.1

## Improvements

- UI improvements to history section.
- Added additional customization options for TCF 2.0 banner.

## Resolved Issues

- Solve thread freeze issue for edge case initialization flow.
- Solved stability issues.

# 2.6.0

## Features

- **[Geolocation Rules]** By initializing our SDK using the Rule Set ID, now you can have your geolocation rules being applied for your mobile app.
- **[Custom UI]** Since we display some fields using HTML, we are now exposing them using Spanned (Android) and NSMutableAttributedString.
- **[Analytics]** To help the integration process, we've created a feature section to further explain how to use Analytics with Custom UI.

## Resolved Issues

- General bug fixes.
- Improve stability and performance issues.

# 2.5.3

## Resolved Issues

    * Fixes issues when parsing TCF String

# 2.5.2

## Resolved Issues

    * TCF String solved issue when signalling legitimate interests

# 2.5.1

## Resolved Issues

    * TCF String solved issue with encoding to shorten the length of the string

# 2.5.0

## Features

- **[UI]** Controller ID section was redesigned to have a better UX.
- `ccpaData` exposes the encoded `uspString`.

## Improvements

- Improve stability and performance issues.

## Resolved Issues

- General bug fixes.
- **[iOS]** Access to `rootViewController` depending on API version.

# 2.4.0

## Features

- **[Customization]** You now have full control over the appearance of the First & Second Layer via our Admin Interface Style options and our Programmatic API. We have updated and extended our Programmatic API to simplify banner customization. 
- **[UI]** Legal links are now added to our the First Layer, and can be hidden or shown as desired via programmatic API.
- **[CCPA]** Consent button can now be customized via the Admin Interface.
- **[API Update]** `tcString` has been deprecated in favor of `tcfData`. This method returns all neccessary data to be consumed related to TCF 2.0 framework.
- **[API Update]** `tcfData` is now async to provide accurate results when actions are still pending to be reflected.

## Improvements

- Improve initialization flow for stability and avoid edge case crashes.
- You may now customize your call to actions: Accept, Deny, Save Buttons independently for First & Second Layer.
- Required updates for TCF 2.0 framework.

## Resolved Issues

- Solve stability issues and bug fixes.
- Issue when showing TCF without any vendors.
- UI/UX improvements and fixes.

# 2.3.0

## Features

- **[API Update]** `shouldShowCMP` has been deprecated in favor of `shouldCollectConsent`. See [Initializing the SDK](https://docs.usercentrics.com/cmp_in_app_sdk/latest/getting_started/initialize/#initializing-the-sdk)
- **[Banner API v2]** Banner API v1 is now discontinued and removed from the SDK. If you don't wish to upgrade, please stick to v2.0.3 to avoid unexpected behaviour. See the [alert in the "Banner API V1" tab](https://docs.usercentrics.com/cmp_in_app_sdk/latest/collect_consent/present_cmp/)
- **[Banner API v2]** BannerSettings now requires a BannerFont object to pass a Bold and Regular font separately to apply for both layers. See [Banner Settings](https://docs.usercentrics.com/cmp_in_app_sdk/latest/collect_consent/customize_cmp/#banner-style-settings)
- **[Demo App]** You can now find a demo app in our documentation to test out your configuration before writing a single line of code. See [Sample Apps](https://docs.usercentrics.com/cmp_in_app_sdk/latest/samples/ios-android-demos/).

## Improvements

- Updates to TCF 2.0 framework.

## Resolved Issues

- Issue with position of logo on Second Layer is now solved.
- UI/UX improvements and fixes.

# 2.2.1

## Features

- **[Banner API v2]** A complete revamp of our banner API will enable you to have high customisation and versatility to build a end-user friendly consent banner. We can't wait for you to give it a try. For more details, see: Presenting the Banner.
    - Add a Header Image to your banner.
    - Have full control over the layour of your action buttons with Column, Row or Grid configurations.
    - Launch the second layer directly.
    - Landscape Mode support.
    - You can now add a "More Information" link to your banner message to forward users to the 2nd Layer. Appearance > Settings > More Information Link in Banner Message. Then you will be able to add this link in the banner message text editor.
- **[Usability]** Collect consent only at a category level. Option available in your Admin Interface: Configure > Legal Specifications > Settings > Category Consent.
- **[CNIL]** "Continue wthout Accepting" feature is now supported. (French regulation)
- **[Fonts]** Admin Interface fonts are now deprecated for App. To enable custom fonts, please inject the font via banner API.

## Improvements

- **[API]** Expose user's consent history.
- **[TCF 2.0]** Adding support to actively inform users when vendors are sharing data outside a region.
- **[CCPA]** Improve API to facilitate compliance with new Banner API.

## Resolved Issues
- **[TCF 2.0]** Minor design upgrades to improve usability.
- **[iOS]** Edge case with RestoreUserSession failing is now solved.
- **[iOS]** Issue with local and remote images losing quality is now solved.
- UI/UX improvements and fixes.

# 2.0.3

- Minor fix on UI related to consent toggles.
- Corner radius on iOS.

# 2.0.2

- Custom UI API.

# 2.0.1

- Initial version of the library.
