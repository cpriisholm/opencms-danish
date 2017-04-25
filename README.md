# opencms-danish
Danish translation of the [OpenCms](http://www.opencms.org) workplace

*In order to build the project with the included **build.gradle**, you need the [opencms gradle plugin](https://github.com/cpriisholm/opencms-gradle-plugin/).*

## Fix for version 10.0.1

OpenCms 10.0.1 is missing a *da.js* file for the tinymce WYSIWYG editor, which results in tinymce not when editing
content for the Danish locale.

Client side fails when trying to load this:

`./WEB-INF/classes/org/opencms/editors/tinymce/static/editors/tinymce/jscripts/tinymce/plugins/codemirror/langs/da.js`

As a workaround use the provided, patched jar: **org.opencms.editors.tinymce.jar**

It includes

`OPENCMS/editors/tinymce/jscripts/tinymce/plugins/codemirror/langs/da.js`

with this content:
```
tinymce.addI18n('da',{
        'HTML source code': 'HTML-kildekde',
        'Start search': 'Find',
        'Find next': 'Find næste',
        'Find previous': 'Find forrige',
        'Replace': 'Erstat',
        'Replace all': 'Erstat alle'
});