# Using the progressive web app (PWA)
While ntfy doesn't have a native desktop app, it is built as a [progressive web app](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps) (PWA)
and thus can be **installed on both desktop and mobile devices**.

This gives it its own launcher (e.g. shortcut on Windows, app on macOS, launcher shortcut on Linux, home screen icon on iOS, and
launcher icon on Android), a standalone window, push notifications, and an app badge with the unread notification count.

Web app installation is **supported on** (see [compatibility table](https://caniuse.com/web-app-manifest) for details):

- **Chrome:** Android, Windows, Linux, macOS
- **Safari:** iOS 16.4+, macOS 14+
- **Firefox:** Android, as well as on Windows/Linux [via an extension](https://addons.mozilla.org/en-US/firefox/addon/pwas-for-firefox/)
- **Edge:** Windows

Note that for self-hosted servers, [Web Push](../config.md#web-push) must be configured for the PWA to work.

## Installation

### Chrome on Desktop
To install and register the web app via Chrome, click the "install app" icon. After installation, you can find the app in your
app drawer:

<div id="pwa-screenshots-chrome-safari-desktop" class="screenshots">
    <a href="../../static/img/pwa-install.png"><img src="../../static/img/pwa-install.png"/></a>
    <a href="../../static/img/pwa.png"><img src="../../static/img/pwa.png"/></a> 
    <a href="../../static/img/pwa-badge.png"><img src="../../static/img/pwa-badge.png"/></a>
</div>

### Chrome/Firefox on Android
For Chrome on Android, either click the "Add to Home Screen" banner at the bottom of the screen, or select "Install app"
in the menu, and then click "Install" in the popup menu. After installation, you can find the app in your app drawer, 
and on your home screen.

<div id="pwa-screenshots-chrome-android" class="screenshots">
    <a href="../../static/img/pwa-install-chrome-android.jpg"><img src="../../static/img/pwa-install-chrome-android.jpg"/></a>
    <a href="../../static/img/pwa-install-chrome-android-menu.jpg"><img src="../../static/img/pwa-install-chrome-android-menu.jpg"/></a>
    <a href="../../static/img/pwa-install-chrome-android-popup.jpg"><img src="../../static/img/pwa-install-chrome-android-popup.jpg"/></a>
</div>

For Firefox, select "Install" in the menu, and then click "Add" to add an icon to your home screen:

<div id="pwa-screenshots-firefox-android" class="screenshots">
    <a href="../../static/img/pwa-install-firefox-android-menu.jpg"><img src="../../static/img/pwa-install-firefox-android-menu.jpg"/></a>
    <a href="../../static/img/pwa-install-firefox-android-popup.jpg"><img src="../../static/img/pwa-install-firefox-android-popup.jpg"/></a>
</div>

### Safari on iOS
On iOS Safari, tap on the Share menu, then tap "Add to Home Screen":

<div id="pwa-screenshots-safari-ios" class="screenshots">
    <a href="../../static/img/pwa-install-safari-ios-button.jpg"><img src="../../static/img/pwa-install-safari-ios-button.jpg"/></a>
    <a href="../../static/img/pwa-install-safari-ios-menu.jpg"><img src="../../static/img/pwa-install-safari-ios-menu.jpg"/></a>
    <a href="../../static/img/pwa-install-safari-ios-add-icon.jpg"><img src="../../static/img/pwa-install-safari-ios-add-icon.jpg"/></a>
</div>

## Background notifications
Background notifications via web push are enabled by default and cannot be turned off when the app is installed, as notifications would
not be delivered reliably otherwise. You can mute topics you don't want to receive notifications for.

On desktop, you generally need either your browser or the web app open to receive notifications, though the ntfy tab doesn't need to be
open. On mobile, you don't need to have the web app open to receive notifications. Look at the [web docs](./web.md#background-notifications)
for a detailed breakdown.
