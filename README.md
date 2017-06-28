# ec-webapps-docs


Table of Contents
=================
1. [Getting Started](#getting-started)
2. [Templates, Layouts and Widgets Explained](#templates-layouts-widgets)
3. [Routing](#routing)
4. [Controls](#controls)

Getting Started
===
To start with, lets create CouchDB database `sample` just with 2 documents inside.

**`--Config`**:
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
Now its time to describe what exactly we will see when navigating to that route.

**`--Template-`**:
```
{
  "_id": "--Template-Sample",
  "type": "template",
  "container": [
    {
      { "type": "Header", "value": "Hello, world" },
      { "type": "Paragraph", "value": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer ac massa at ex eleifend iaculis sed scelerisque sem. Quisque facilisis orci dolor, vel interdum purus tincidunt sed. Quisque pharetra libero at augue luctus, at pharetra felis dignissim. Phasellus hendrerit arcu sed tellus imperdiet, at ultrices lorem molestie. Ut non fringilla lorem. Nulla interdum mauris et lectus vestibulum vestibulum. Praesent et mauris ultrices turpis finibus pharetra." }
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



