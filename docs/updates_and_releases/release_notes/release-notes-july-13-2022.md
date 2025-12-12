---
description: 
---

# Release Notes - July 13, 2022

# New Features

  * The following apps are now supported in Cerby with automatic login:
    * Loom
    * Radware Cloud
    * Panacea (Threat Grid)
    * Arbor Sightline
    * ThreatConnect
    * Fortinet
    * Arbor Technical Assistance Center
    * Cisco Digital Learning
    * Zoom
    * Arelion
    * New York Times
    * Wall Street Journal
    * Later
    * Reddit
    * Hubspot
    * Netflix
    * Tumblr
    * Chicago Tribune
    * GoDaddy
    * Similarweb
  * Automatic swap email is now supported for Reddit and Tumblr.
  * Password rotation policies are now available for Instagram and Pinterest.
  * Automatic MFA enrollment is now supported for Snapchat using the Cerby mobile application; with the Cerby web application is now supported automatic password rotation.
  * The TikTok Business and TikTok Ads roles are now mapped in Cerby.
  * Automatic password rotation is now supported for Domo.
  * Users are now notified through email when something unexpected happens during a password manager importer migration.
  * Automatic MFA offboarding is now supported for Instagram using the Cerby mobile application.
  * Pixel assets are now supported for Facebook Business Manager accounts in Cerby.

# Fixes

  * The issue with updating the password for a Pinterest account through the **Edit Account Details** page is fixed.
  * The issue with logging in automatically to a Later account using Firefox is fixed.
  * The issue with turning on MFA automatically when validating a Cerby-managed email address or phone number before requesting a verification code is fixed.
  * The issue with validating a Cerby-managed phone number when rotating a password automatically in TikTok is fixed.
  * The issue with turning on MFA automatically for a Twitter account is fixed.
  * The issue with Canva constantly refreshing after logging in through Cerby using Firefox is fixed.
  * The issue with logging in automatically to an Instagram account when a user has a Facebook session active is fixed.
  * The issue with logging in automatically to a Canva account is fixed.
  * The issue with authenticating to a TikTok account through the Chrome browser extension is fixed.
  * The issue with expanding TikTok assets from the **More** button of the **All Members** view is fixed.
  * The issue with the final results page in the **Policies** view displaying an incorrect empty state is fixed.
  * The issue with removing Facebook Business Manager users from the **All Members** view when an account is included in a collection is fixed.
  * The issue with the unexpected timeout when logging in automatically to Similarweb, Later, and Canva accounts is fixed.

# Security Fixes

  * A potential click-jacking configuration issue with the [www.cerby.com](http://www.cerby.com) site is fixed. Discovery credit: Sakshi Patil.
