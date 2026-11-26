# Desktop location, time zone and Chrome language

Use the controls on the desktop where Chrome runs. Record the existing master switch and time zone before changing them. The time zone affects every app on the computer. Keep automatic clock synchronization enabled if it was enabled. Use a named zone with the appropriate daylight-saving rules. If geolocation returns only a city, a country or a UTC offset, leave the current zone in place and report the missing information.

## macOS

- **Location.** System Settings → Privacy & Security → Location Services. Turn off the master switch and verify it after closing and reopening the pane. [Apple Location Services](https://support.apple.com/guide/mac-help/control-access-to-the-location-of-your-mac-mh35873/mac)
- **Time zone and city.** System Settings → General → Date & Time. Turn off automatic time zone selection and enter the exit city in **Closest city**. If it is unavailable, select a listed city in the verified IANA zone. Reopen the pane and verify the resulting zone. This city controls the clock. macOS provides no system control here to supply a replacement device position to websites. [Apple Date & Time settings](https://support.apple.com/guide/mac-help/change-date-time-settings-mchlp1124/mac)
- **Chrome menus.** System Settings → General → Language & Region → Applications. Add or edit Google Chrome and select English. This affects Chrome across this macOS user's profiles. Relaunch when the user can close their Chrome windows, then reopen the intended profile and verify its menus. [Apple per-app languages](https://support.apple.com/guide/mac-help/change-the-system-language-mh26684/mac)

## Windows 11

- **Location.** Settings → Privacy & security → Location → **Location services** → Off. Verify the device-wide control. Windows' default location is a fallback when a precise location is unavailable. With Location services off, report the IP-derived city separately. [Microsoft location settings](https://support.microsoft.com/en-us/windows/privacy/windows-location-service-and-privacy)
- **Time zone.** Settings → Time & language → Date & time. Turn off **Set time zone automatically**, then select the Windows zone corresponding to the verified IANA zone. If the mapping is ambiguous, consult Unicode's territory-aware mapping. Reopen the pane or run `Get-TimeZone` to verify. [Microsoft Date & time](https://support.microsoft.com/en-us/windows/experience/personalization/set-time-date-and-time-zone-settings-in-windows) · [Unicode time-zone mapping](https://github.com/unicode-org/cldr/blob/main/common/supplemental/windowsZones.xml)
- **Chrome menus.** In `chrome://settings/languages`, use the English entry's menu, choose **Display Google Chrome in this language**, relaunch when convenient, and verify. [Chrome language settings](https://support.google.com/chrome/answer/173424?hl=en)

## Linux desktop

- **Location.** In GNOME open Settings → Privacy & Security → Location and turn off **Automatic Device Location**. Verify the control. For other desktops use their documented equivalent if available and report its scope. [GNOME location](https://help.gnome.org/gnome-help/privacy-location.html)
- **Time zone.** GNOME Settings → System → Date & Time → Automatic Time Zone off → Time Zone. Select a city in the verified zone and reopen the pane. On a systemd host, `timedatectl show --property=Timezone --value` provides a readback. [GNOME time zone](https://help.gnome.org/gnome-help/clock-timezone.html)
- **Chrome menus.** Set preferred content to English in the profile. Linux Chrome normally follows the desktop locale for menus. When all Chrome processes have been closed normally, start the installed Chrome executable with the process environment `LANGUAGE=en_US` for an English launch. Verify the menus in the intended profile. If the user wants this on every launch, use a per-user Chrome launcher with that environment setting. [Chrome language settings](https://support.google.com/chrome/answer/173424?hl=en) · [Chromium locale selection](https://chromium.googlesource.com/chromium/src/+/main/ui/base/l10n/l10n_util.cc)
