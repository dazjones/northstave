---
title: "Adding an iCloud Calendar to Thunderbird"
date: 2024-08-06
description: "To synchronize your iCloud calendar with Thunderbird, you need to obtain the correct CalDAV URL and configure it in Thunderbird's calendar settings"
tags: ["icloud", "thunderbird", "linux"]
---
To synchronize your iCloud calendar with Thunderbird, you need to obtain the correct CalDAV URL and configure it in Thunderbird's calendar settings. This guide provides detailed steps for both retrieving the necessary URL and setting up Thunderbird.

## Prerequisites

- **Mozilla Thunderbird**: Ensure you have Thunderbird installed on your system.
- **Provider for CalDAV & CardDAV**: This Thunderbird add-on helps manage CalDAV calendars and CardDAV address books.
- **Apple ID**: The email and password for your iCloud account.

## Retrieving the iCloud Calendar URL

To add an iCloud calendar to Thunderbird, you'll first need the specific CalDAV URL. Follow these steps:

### Method A: Obtain a Session Token from iCloud

1. **Login to iCloud:**
   - Open a web browser and navigate to [iCloud.com](https://www.icloud.com).
   - Log in using your Apple ID and password.

2. **Inspect Web Traffic:**
   - Once logged in, right-click anywhere on the page and select "Inspect" or press `Ctrl + Shift + I` (Windows/Linux) or `Cmd + Option + I` (Mac) to open the developer tools.
   - Go to the "Network" tab. If this tab isn't visible, it might be under "More Tools."

3. **Access iCloud Calendar:**
   - Click on the Calendar icon within iCloud.

4. **Filter for "CalDAV" Requests:**
   - In the Network tab, filter the requests by typing "caldav" in the search box. You're looking for requests that include your calendar data.

5. **Find the CalDAV URL:**
   - Look for a request containing "caldav" in the "Name" column. Click on it.
   - In the "Headers" tab, under "Request URL," you should see the CalDAV URL. It usually looks like:

     ```
     https://pXX-caldav.icloud.com/1234567890/calendars/primary/
     ```

   - Copy this URL for use in Thunderbird.

### Method B: Alternative Method Using Calendar App URL

1. **Open Calendar Settings:**
   - In iCloud Calendar, click on the share icon next to the calendar you want to add (a Wi-Fi-like icon).
   - Ensure the calendar is set to "Public." This is temporary, as you'll switch it back to private after obtaining the URL.

2. **Copy the Calendar URL:**
   - Once public, a URL will appear. Copy this URL. It will look like:

     ```
     webcal://pXX-caldav.icloud.com/1234567890/calendars/primary.ics
     ```

3. **Modify the URL:**
   - Change "webcal" to "https" and remove the `.ics` at the end. The modified URL should look similar to:

     ```
     https://pXX-caldav.icloud.com/1234567890/calendars/primary/
     ```

## Adding iCloud Calendar to Thunderbird

Now that you have the CalDAV URL, follow these steps to add it to Thunderbird:

1. **Install the Provider for CalDAV & CardDAV Add-on:**
   - Open Thunderbird.
   - Go to the "Menu" (≡) > "Add-ons and Themes".
   - Search for "Provider for CalDAV & CardDAV".
   - Click "Install".

2. **Add New Calendar:**
   - In Thunderbird, go to "Events and Tasks" > "Calendar" (or press `Ctrl + Shift + C`).
   - Right-click in the left calendar pane and select "New Calendar...".
   - Choose "On the Network" and click "Next".

3. **Configure CalDAV Calendar:**
   - Select "CalDAV".
   - In the "Location" field, paste the CalDAV URL you obtained earlier.
   - Click "Next".

4. **Authentication:**
   - Enter your Apple ID credentials when prompted.

5. **Complete Setup:**
   - Assign a name to your calendar.
   - Choose a color if desired.
   - Set any other preferences, then click "Next" and "Finish".

## Verifying Calendar Sync

- The calendar should now appear in Thunderbird. Ensure that events from iCloud are visible and new events created in Thunderbird sync to iCloud.

## Re-secure Your iCloud Calendar (Optional)

If you set your calendar to public to obtain the URL, you can now set it back to private:

1. Go back to [iCloud.com](https://www.icloud.com) > Calendar.
2. Click the share icon next to the calendar.
3. Uncheck the "Public Calendar" option.

## Troubleshooting

- **Incorrect URL Error:** Ensure the URL does not include `.ics` at the end and uses `https`.
- **Authentication Issues:** Double-check your Apple ID credentials.
- **Sync Delays:** It may take a few minutes for changes to reflect. Ensure Thunderbird is online and connected.

## Additional Tips

- **Multiple Calendars:** Repeat the process for additional calendars.
- **Event Notifications:** Configure Thunderbird's notification settings to match your preferences.
