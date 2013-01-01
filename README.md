# openwebcraft.com

The [openwebcraft.com][openwebcraft.com] web site (builder).

## Building Blocks

- **Application platform**: [Node.js][nodejs] - event-driven I/O server-side JavaScript environment based on [V8][v8] (Chrome's JavaScript runtime).

- **Builder application**: [static+][static-plus] -  Static web site and web application builder.

- **Builder backend**: [CouchDB][couchdb] - a (NoSQL) database
that uses JSON for documents, JavaScript for MapReduce queries, and regular HTTP for an API.

- **Text formatting**: [markdown][markdown] - plain text formatting syntax and text-to-HTML conversion tool for web writers.

- **Templates**: [Handlebars.js][handlebarsjs] - Minimal Templating on Steroids.

## Heroku Deployment Steps

Install the [Heroku Toolbelt][heroku-toolbelt] - everything you need to get started using heroku.

Authenticate/ login: `heroku login`

Install [heroku-config][heroku-config], a plugin for the `heroku` CLI that makes it easy to *push* or *pull* your application’s config environment vars, from or into your local `.env` file.

Create a `.env` file with your project configuration:

    COUCH_SERVER=https://ADMIN:PASSWORD@EXAMPLE.iriscouch.com
    COUCH_DB=example_com
    DOMAIN=example.com
    SP_PREFIX=
    SP_STAGING_PREFIX=staging.
    SP_BOUNCE_PREFIX=www.
    SP_SEED=./tpl
    SP_PUBLISH=./assets

Push your local environment file to Heroku: `heroku config:push`

Next, deploy the application to Heroku.

Create the app: `heroku create`

Deploy the code: `git push heroku master`


[openwebcraft.com]: http://openwebcraft.com "openwebcraft.com"
[static-plus]: https://github.com/iriscouch/static-plus "static+"
[couchdb]: http://couchdb.apache.org "CouchDB"
[nodejs]: http://nodejs.org "Node.js"
[v8]: http://code.google.com/p/v8/ "V8 JavaScript Engine"
[markdown]: http://daringfireball.net/projects/markdown/ "Markdown"
[handlebarsjs]: http://handlebarsjs.com "Handlebars.js"
[heroku-toolbelt]: https://toolbelt.heroku.com "heroku toolbelt"
[heroku-config]: https://github.com/ddollar/heroku-config "heroku-config"

