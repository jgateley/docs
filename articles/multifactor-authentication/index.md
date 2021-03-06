---
title: Multifactor Authentication in Auth0
description: The basics of multifactor authentication and the different methods of implementing it with Auth0.
url: /multifactor-authentication
---

# Multifactor Authentication in Auth0

Multifactor Authentication (MFA) is a method of verifying a user's identity by requiring them to present more than one piece of identifying information. This method provides an additional layer of security, decreasing the likelihood of unauthorized access. The type of information required from the user is typically two or more of the following:

* **Knowledge**: Something the user knows (such as a password)
* **Possession**: Something the user has (such as a cell phone)
* **Inheritance**: Something the user is (such as a fingerprint or retina scan)

## Implementing MFA with Auth0

Auth0 supports the following methods of implementing MFA:

1. [Push Notifications (Auth0 Guardian)](/multifactor-authentication#mfa-using-push-notifications-auth0-guardian-) - Auth0's mobile application Guardian sends push notifications for MFA
2. [SMS (Auth0 Guardian)](/multifactor-authentication#mfa-with-sms) - Verification by sending a six-digit code via SMS
3. Support for one-time password authentication services [Google Authenticator](/multifactor-authentication#mfa-using-google-authenticator) and [Duo Security](/multifactor-authentication#mfa-using-duo-security).
4. [Configuring rules for custom processes](/multifactor-authentication#mfa-using-custom-rules) - such as Contextual MFA, which allows you to define the conditions that will trigger additional authentication challenges, such as changes in geographic location or logins from unrecognized devices.
5. Using a [custom provider](/multifactor-authentication#mfa-using-a-custom-provider), such as **Yubikey**.

## MFA using Push Notifications (Auth0 Guardian)

<div class="phone-mockup"><img src="/media/articles/mfa/guardian-push.png" alt="Guardian Push Screenshot"/></div>

Guardian is Auth0's MFA application. It is a frictionless approach to implementing MFA for your apps, and provides a full MFA experience without requiring integration with third-party utilities.

[Click here to learn more about enabling push notifications with Guardian](/multifactor-authentication/guardian)

## MFA with SMS

<div class="phone-mockup"><img src="/media/articles/mfa/sms-screenshot.png" alt="MFA SMS Screenshot"/></div>

Auth0 supports sending an SMS with a one-time password code to be used for another step of verification.

[Click here to learn more about enabling SMS](/multifactor-authentication/guardian/admin-guide#support-for-sms)

## MFA Using Google Authenticator

<div class="phone-mockup"><img src="/media/articles/mfa/google-auth-screenshot.png" alt="Screenshot of Google Authenticator"/></div>

Google Authenticator is a mobile app that generates 2-step verification codes. This creates a one-time use password that is used as the second factor after your user has attempted to log in with their Google credentials.

[Click here to learn more about enabling Google Authenticator](/multifactor-authentication/google-authenticator)

## MFA Using Duo Security

<div class="phone-mockup"><img src="/media/articles/mfa/duo-screenshot.png" alt="DUO Screenshot"/></div>

Duo Security allows you to request either of the following as your second factor once the user has provided their initial login credentials:

* A user response to a push notification sent to the appropriate device
* A passcode provided to the user via SMS

[Click here to learn more about enabling Duo](/multifactor-authentication/duo)

## MFA Using Custom Rules

You may [configure rules](/rules) for custom MFA processes, which allow you to define the conditions that will trigger additional authentication challenges, such as changes in geographic location or logins from unrecognized devices.

[Click here for sample code snippets](/multifactor-authentication/custom) to assist you in building your rules here.

## MFA Using a Custom Provider

For a detailed look at implementing a custom MFA provider, see [Multifactor Authentication with YubiKey-NEO](/multifactor-authentication/yubikey) as an introduction.

## User-initiated MFA

For details on how to implement user-initiated MFA, so you can flag users for MFA as part of the user creation/login process, refer to [User-Initiated Multifactor Authentication](/multifactor-authentication/user-initiated-mfa).
