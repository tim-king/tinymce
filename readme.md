TinyMCE - The JavaScript Rich Text editor
==========================================

Offline tinymce
---------------
The standard tinymce creates an iframe with no src. This means that when you try to load CSS inside it they aren't cached by Service Workers, and hence won't work offline. All of tinymce itself is cached, just not the CSS it inserts into the iframe.

This tiny workaround lets you specify an option editor_file that should point to a (probably) blank file on your current domain. This is specified as the src of the iframe, and now any CSS added is from the initial domain so the Service Worker will match the domain and if you have set that up right you can edit a file offline.

You have to set the save file stuff to work offline of course - that's up to you.
The main tinymce repo is at
```
https://github.com/tinymce/tinymce.git
```
