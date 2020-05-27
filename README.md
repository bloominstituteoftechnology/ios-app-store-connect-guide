# Lambda App Store Connect Guide

At the beginning of Unit 3 in iOS Core, you will be sent an invite to join the Lambda School Apple Developer program account. This invite will be sent to your lambdastudents.com email address.

If you don't receive an email at the start of Unit 3, check the following:

1. Check your junk mail to be sure it didn't end up there. This is the most common reason why students don't see the invitation email.
2. If you are still experiencing issues, reach out to your TL, SL, or Instructor for additional assistance.

## Overview for *All* Student Developers

You will work on an iOS app that likely other students have worked on before. If so, an app instance will already exist in Lambda's Apple Developer account.

### Certificate Installation

1. Download Lambda School's distribution certificate to your compputer. This file will be sent to your class in your private class channel at the start of Build Week in Unit 3 (uploading to TestFlight is recommended but not required in Unit 3, and required in Unit 4).
    * The filename for this certificate will look like this: `Lambda_Shared_Apple_All_Platforms_Distribution_Certificate.p12`
2. Double click this file to install in your Mac's Keychain.
    * The Keychain app will ask for a password to install this certificate. Look for the password alongside the file in your cohort's class channel.

### Provisioning Profile Installation

3. Please fill out [this form](https://forms.gle/Uom2CMpSosmJH87j6) after your Build Week kickoff meeting. **You must fill out this form *once per team*.**
3. Each app that gets uploaded to App Store Connect (the interface Apple provides for testing and distributing iOS apps) needs a provisioning profile. This file is unique to the Apple Developer account and to the app itself. When you filled out the form above, you provided name for the app you're working on for Build Week as well as the *bundle identifier*. Make sure the bundle ID from the form is the same as what's listed in Xcode's project properties screen.
    * Your instructor will provide each team with a provisioning profile for your app in Slack. The file will look something like this: `AppName_App_Store_Provisioning_Profile.mobileprovision`, where `AppName` is the name of your app project.
4. Once the above file is downloaded to your Mac, open your Xcode project and go to the Xcode project properties screen (the blueprint icon in the file navigator). Click into the tab marked **Signing & Capabilities**.
5. Uncheck the box marked *Automatically manage signing*. This will generate an error in the status field of this screen.
![Xcode signing config](https://raw.githubusercontent.com/LambdaSchool/ios-app-store-connect-guide/master/Assets/Images/xcode-import-profile.png)
6. Click the dropdown menu marked *Provisioning Profile* and choose **Import Profile...**
7. Choose from your filesystem the `.mobileprovision` file you downloaded in step 3.

Your project is now configured to upload builds to TestFlight.

NOTE: The version number listed in your project is probably `1.0`, which is fine. The build number however must be unique for each build you upload to TestFlight. The first one will probably be build `1`, but if previous students have worked on this app, the number could be higher. Check with your TL to find out what appropriate build number should be used before following the steps below to upload to TestFlight.
![Xcode version and build config](https://raw.githubusercontent.com/LambdaSchool/ios-app-store-connect-guide/master/Assets/Images/xcode-version-build.png)

### Upload a Build to TestFlight

* Follow the steps outlined by Apple [here](https://help.apple.com/xcode/mac/current/#/dev2539d985f) to upload a build to TestFlight. Please ask your TL, SL, or an instructor for help if you get stuck.
* Once you upload the build from Xcode, please notify your TL or an instructor as there are a couple steps we need to complete for you to get your build approved for testing. When you contact us, please provide the following information:
    * an email address for beta testers to send you feedback
    * a phone number and email (might be same as above) that the App Store Review team can contact you at if they need to (they very likely won’t contact you)
    * Does your app require a login to use? If so, you must provide a username and password pre-made to give to the review team. They will not create an account on their own.
    * a list of features you’d like your beta testers to check out in the app (this text is tester-facing, so it would show up for anyone who uses the link to install the app).
* After providing this information to your TL or an instructor, we'll submit your app for approval and once approved (usually takes 24 hours or so), we'll provide you with a link you can give testers to check out your app.