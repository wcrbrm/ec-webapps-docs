# ec-webapps-docs


Table of Contents
=================
1. [Getting Started](#getting-started)
2. [Templates, Layouts and Widgets Explained](#templates-layouts-widgets)
3. [Routing](#routing)
4. [Controls](#controls)

Getting Started
===
To start with, lets create CouchDB database with 2 documents
*`--Config`*:
```
{
  "_id": "--Config",
  "type": "webapp-config",
  "website": {
    "title": "Sample Application"
  },
  "routes": [
    {
      "path": "/",
      "template": "Sample",
      "title": "Sample Application"
    }
  ]
}
```

That was a confuguration document, mainly with routing configuration.
*`--Template-`*:
```
{
  "_id": "--Template-Sample",
  "type": "template",
  "container": [
    {
    }
  ]
}
```

Templates, Widgets and Layouts Explained
===
TBD...

Routing
===
TBD...

Controls
===
TBD...



