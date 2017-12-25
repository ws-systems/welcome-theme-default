Welcome Default Theme
=====================

Client Kiosk Templates are located in the `client` directory, while the Quick
Clock templates are located in the `qc` directory. Styles and JS for the theme
can be found in the `theme` folder, and should be referenced as such from the
templates themselves, using absolute references, like shown below, wherever
possible.

### Referencing Theme Assets
If we want to reference a JS script located in `themes/js/main.js`, we would
reference the file as follows to ensure that Welcome can properly serve the
correct theme assets for the site. Failing to include the first `/` can cause
the reference to not load correctly.

```html
<script type="application/javascript" src"/theme/js/main.js"></script>
```

### Building Themes
For both Client Interfaces and Quick Clock Interfaces, in the `client` and `qc`
folders respectively, the `index.twig` file will be loaded by Welcome on site
load. The index file is responsible for loading all of the other required
assets, either via twig functions, or `<link>` or `<script>` tags. All designs
must be "one-page," and cannot change URL while in the interface.

### TODO
- Add thumbnail image
- Add License info to meta.json
- Add Standard for meta.json
