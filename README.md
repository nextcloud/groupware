# Groupware

Meta repo for the groupware team

The purpose of this repo is primarily to be able to create tickets for tasks that span across the groupware repos.

## Scope and purpose

The Groupware team is dedicated to improving and maintaining all groupware aspects inside the Nextcloud ecosystem.

### Members

* [Anna Larch](https://github.com/miaulalala)
* [Christoph Wurst](https://github.com/ChristophWurst)
* [Daniel Kesselberg](https://github.com/kesselb)
* [Greta Doçi](https://github.com/GretaD)
* [Grigory Vodyanov](https://github.com/GVodyanov)
* [Hamza](https://github.com/hamza221)
* [Pablo](https://github.com/pabzm)
* [Richard Steinmetz](https://github.com/st3iny)
* [Sebastian Krupinski](https://github.com/SebastianKrupinski)
* [Thomas Citharel](https://github.com/tcitworld)

### Components and roles

The code and information is spread across multiple repositories. The following list shows where the main bits and pieces can be found, and who is responsible.

| Component | Maintainers | Release manager |
|-----------|-------------|-----------------|
| [CalDAV and CardDAV backends](https://github.com/nextcloud/server/tree/master/apps/dav) | Richard, Sebastian | Server team |
| [Calendar](https://github.com/nextcloud/calendar) | Richard, Sebastian, Thomas | Sebastian |
| [Calendar Resource Management](https://github.com/nextcloud/calendar_resource_management) | Richard, Sebastian | Richard |
| [Contacts](https://github.com/nextcloud/contacts) | Grigory, Hamza, Sebastian | Hamza |
| [Contacts Interaction](https://github.com/nextcloud/server/tree/master/apps/contactsinteraction) | Daniel, Sebastian | Server team |
| [Mail](https://github.com/nextcloud/mail) | Christoph, Daniel, Greta | Christoph |
| [`@nextcloud/calendar-availability-vue`](https://github.com/nextcloud/calendar-availability-vue ) | Greta, Grigory | Greta |
| [`@nextcloud/calendar-js`](https://github.com/nextcloud/calendar-js) | Grigory, Richard | Grigory |
| [`@nextcloud/cdav-library`](https://github.com/nextcloud/cdav-library) | Hamza, Richard | Richard |
| [`@nextcloud/timezones`](https://github.com/nextcloud-libraries/timezones) | Greta, Richard | Richard |
| [`nextcloud/kitinerary`](https://github.com/nextcloud-libraries/kitinerary) | Christoph, Daniel | Daniel |
| [`nextcloud/kitinerary-bin`](https://github.com/nextcloud-libraries/kitinerary-bin) | Christoph, Daniel | Daniel |
| [`nextcloud/kitinerary-flatpak`](https://github.com/nextcloud-libraries/kitinerary-flatpak) | Christoph, Daniel | Daniel |
| [`nextcloud/kitinerary-sys`](https://github.com/nextcloud-libraries/kitinerary-sys) | Christoph, Daniel | Daniel |
| [Roundcube](https://github.com/roundcube/roundcubemail) | [Alec](https://github.com/alecpl), Pablo, Anna | [Alec](https://github.com/alecpl), Pablo |

#### Roles explained

* **Maintainers** actively manage issue reports, review and merge pull requests and backport critical fixes. They are explicit *code owners* on Github.
* **Release managers** ensure that changes are released at the right time, e.g. in short time frame for fixes, or at defined dates for features.
