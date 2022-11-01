2019.0 (2019-12-13): First public release.

2020.0 (2020-01-24): Introduce LDAP support to map email addresses to login IDs.

2020.1 (2020-03-08): Support "werkzeug" release 1.0.0.

2020.2 (2020-12-16): Introduce support for POP3 servers.

2021.0 (2021-01-09): Improve handling of login name placeholders in Outlook generator.

2021.1 (2021-02-23): Fix LDAP attribute processing when using Active Directory backends.

2021.2 (2021-03-07): Change XML root element namespace in Outlook generator.

2021.3.1 (2021-04-02): Support additional mixed-case route in Outlook generator. Support CalDAV/CardDAV for eM Client.

2021.4 (2021-04-20): Bugfix: "SSL" element now depends on socket_type DB column. Drop "AuthRequired" XML element from Autodiscover response because automx2 always returned "on", which is the default value if the element is absent.

2021.5 (2021-10-04): Existing versions of automx2 return "do not use SSL" for socket types other than SSL and STARTTLS. This previously undocumented behaviour can cause unexpected results. Future automx2 versions will terminate automx2 when encountering invalid socket type strings in the database. The current release logs an error to notify users of the upcoming change. This release also improves the Mobileconfig generator, making it smarter when choosing among multiple servers defined in the database.

2021.6 (2021-12-17): Introduce "Encryption" element (see MS-OXDSCLI v20210817) in Autodiscover generator to better support server connections which require the use of STARTTLS.

2022.0 (2022-03-31): Simplified database initialisation is now possible via HTTP POST and a JSON payload.

2022.1 (2022-05-20): Request content type verification now works if additional parameters like "charset" are passed.

2022.2, 2022.3, 2022.4: Unpublished releases

2022.5 (2022-10-31): Fork automx2 to automua. First automua public release. Avoid GPLv3 violation. Open project to contributors. Fix the database initialisation w/ HTTP POST & JSON payload (`automua/database.py`). Replace the deprecated setup.py by pyproject.toml. Use hatch to build and publish releases on Python PyPI. Packages for Arch Linux AUR and Python PyPI. Update docs and fix a few contrib files.  