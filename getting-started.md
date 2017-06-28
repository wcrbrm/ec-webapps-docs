
Getting Started
===
To start with, lets create CouchDB database `ecsample` just with 2 documents inside.
You can just manually do that in its interface `http://localhost:5984/_utils/#/` from your browser.

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

**`--Template-Sample`**:
```
{
  "_id": "--Template-Sample",
  "type": "template",
  "container": [
    { "type": "Header", "value": "Hello, world" },
    { "type": "Paragraph", "value": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer ac massa at ex eleifend iaculis sed scelerisque sem. Quisque facilisis orci dolor, vel interdum purus tincidunt sed. Quisque pharetra libero at augue luctus, at pharetra felis dignissim. Phasellus hendrerit arcu sed tellus imperdiet, at ultrices lorem molestie. Ut non fringilla lorem. Nulla interdum mauris et lectus vestibulum vestibulum. Praesent et mauris ultrices turpis finibus pharetra." }
  ]
}
```
Our database is ready.
On the next step, lets create the application itself. The fastest way to have it - is to use [`create-react-app` boilerplate from Facebook Incubator](https://github.com/facebookincubator/create-react-app):  

```
npm install -g create-react-app
create-react-app ec-first-app
```
Then inside of `node_modules` you can download and unpack **the library**
[ec-react15-lib](https://dist.webcerebrium.com/ec-react15-lib.zip). This step should be more seamless in future

To have the simplest example working, you can clean up all files in `src` folder, leaving only `src/index.js` with the following contents:

```
import ec from 'ec-react15-lib';
ec.start({
  baseUrl: 'http://localhost:5984/ecsample',
  preloadUrl: 'http://localhost:5984/ecsample/_all_docs?include_docs=true'
});
```
and launch the application with `npm run start` command. It should be open in browser on a random port
