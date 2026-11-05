# Groupware

Meta repo for the groupware team

The purpose of this repo is primarily to be able to create tickets for tasks that span across the groupware repos.

## Scope and purpose

The Groupware team is dedicated to improving and maintaining all groupware aspects inside the Nextcloud ecosystem.

### Members

* [Christoph Wurst](https://github.com/ChristophWurst)
* [Daniel Kesselberg](https://github.com/kesselb)
* [David Dreschner](https://github.com/derdreschner)
* [Greta Doçi](https://github.com/GretaD)
* [Grigory Vodyanov](https://github.com/GVodyanov)
* [Hamza Mahjoubi](https://github.com/hamza221)
* [Oleksandr Dzhychko](https://github.com/odzhychko)
* [Sebastian Krupinski](https://github.com/SebastianKrupinski)

### Components and roles

The code and information is spread across multiple repositories. The following list shows where the main bits and pieces can be found, and who is responsible.

| Component | Maintainers | Release manager |
|-----------|-------------|-----------------|
| [CalDAV and CardDAV backends](https://github.com/nextcloud/server/tree/master/apps/dav) | Sebastian, Hamza | Server team |
| [Calendar](https://github.com/nextcloud/calendar) | Sebastian, Grigory, Oleksandr | Sebastian |
| [Calendar Resource Management](https://github.com/nextcloud/calendar_resource_management) | Sebastian, Oleksandr | Sebastian |
| [Contacts](https://github.com/nextcloud/contacts) | Hamza, Grigory, Oleksandr | Hamza |
| [Contacts Interaction](https://github.com/nextcloud/server/tree/master/apps/contactsinteraction) | Daniel, Sebastian | Server team |
| [Mail](https://github.com/nextcloud/mail) | Christoph, Daniel, David, Greta | Christoph |
| [`@nextcloud/calendar-availability-vue`](https://github.com/nextcloud/calendar-availability-vue ) | Greta, Grigory | Greta |
| [`@nextcloud/calendar-js`](https://github.com/nextcloud/calendar-js) | Grigory, Sebastian | Grigory |
| [`@nextcloud/cdav-library`](https://github.com/nextcloud/cdav-library) | Hamza, Sebastian | Hamza |
| [`@nextcloud/timezones`](https://github.com/nextcloud-libraries/timezones) | Oleksandr, Sebastian | Oleksandr |
| [`nextcloud/kitinerary`](https://github.com/nextcloud-libraries/kitinerary) | Christoph, Daniel | Daniel |
| [`nextcloud/kitinerary-bin`](https://github.com/nextcloud-libraries/kitinerary-bin) | Christoph, Daniel | Daniel |
| [`nextcloud/kitinerary-flatpak`](https://github.com/nextcloud-libraries/kitinerary-flatpak) | Christoph, Daniel | Daniel |
| [`nextcloud/kitinerary-sys`](https://github.com/nextcloud-libraries/kitinerary-sys) | Christoph, Daniel | Daniel |
| [Suspicious Login](https://github.com/nextcloud/suspicious_login) | David, Christoph | Server team |

#### Roles explained

* **Maintainers** actively manage issue reports, review and merge pull requests and backport critical fixes. They are explicit *code owners* on Github.
* **Release managers** ensure that changes are released at the right time, e.g. in short time frame for fixes, or at defined dates for features.
