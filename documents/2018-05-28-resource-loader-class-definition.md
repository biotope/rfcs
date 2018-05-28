- Start Date: 2018-05-28
- RFC PR: https://github.com/biotope/rfcs/pull/1
- Project: https://github.com/biotope/biotope-resource-loader

# Summary

The resource loader is currently a self executing js file written in jquery, controlled by events. As soon as one includes the resource loader, jquery is needed and the script is run.

# Motivation

The resource loader should not be self executing, but the developer should choose by himself when to access and initialize it.
In addition all of this can be written without the use of jQuery and events.

# Detailed design

## Implementing

We will have a creator function like ```createDynamicResourceLoader``` which will instantiate a resource loader.
The result of this function can then be stored as the developer wishes.

## Using

An example:

```js
window.biotope.resourceLoader = new ResourceLoader();

window.biotope.resourceLoader.on('main.js/loaded', () => {);

window.biotope.resourceLoader.loadDomReferences();
```

# Drawbacks

Besides the cleaner code, it will give the developer more responsibility.
As instantiating the loader in the wrong place may crash the logic. (i.e. two resource loaders by accident)

# Alternatives

1. Leave as is

# Unresolved questions

How does the interface exactly look like?
