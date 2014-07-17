GitHub Digests (GD) is a system that aggregates its users GitHub notifications into daily email digests. This might be really helpful for people who receive dozens or hundreds of notifications per day and actually want to scan the contents of those notifications but don’t need to see each one discretely in realtime.

GD has a few discrete components; each has its own Git repository. *This* repository exists to host documentation for the overall system.

## Components & Repositories

* [github-digests-web](https://github.com/aviflax/github-digests-web) is the Web UI for GD. It serves the public Website and allows people to sign in, adjust their settings, etc. It saves accounts and their settings to the database.
* [github-digests-digester](https://github.com/aviflax/github-digests-digester) is the process that runs hourly, retrieves notifications from GitHub’s API, aggregates them into digest emails, and sends those emails. It retrieves accounts and their settings from the database and saves logs to the database.
* *The database* is a [RethinkDB](http://rethinkdb.com) database. It stores accounts and their settings, and logs. There’s currently no repository for this component because at the moment it’s a 100% stock instance of ReThinkDB with no schema, migrations, secondary indices, or other configuration. If and when those things are necessary, a repository will be created for them.

## Disclaimer

This project is not affiliated or associated with or endorsed by GitHub (the organization). It employs GitHub’s API in conformance with its terms of service.

## Feedback

If you have any questions, suggestions, concerns, or problems to share, please [open an issue](https://github.com/aviflax/github-digests/issues/new) or [email me](mailto:avi+gd@aviflax.com?subject=GitHub+Digests+Rocks).

## License

This entire system is copyright © 2014 by Avi Flax and is licensed under the terms of the MIT License. See [LICENSE](LICENSE) for the full terms.
