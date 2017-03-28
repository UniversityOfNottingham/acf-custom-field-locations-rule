# ACF Custom Field Location Rules

Set ACF field group location based on select, checkbox, radio and true/false fields in other field groups.

## How to use

Create a field group with choice fields.

When adding additional field groups the choice fields in other field groups will be detected 
and be available to chooose from.

* Only top level choice fields are available.
* Repeaters and flexible content sub fields cannot be used.
* The field that you are basing your location rule on must be in a field group on the same post. Any choice field can be selected but if it's not part of another field group on the same post then it woun't do anything.

## Issues with the plugin

It may slow down the loading of admin pages. Every choice field will trigger ACF to run AJAX to check for
field groups to be shown. Worse than this, it will trigger this action for every choice in a radio or
checkbox field. I'm not sure there's anything I can do to change this.

Overall, using this plugin is probably a bad idea for any site that has a large number of field groups with large
numbers of select fields. This puts a heavy burden on page loading when many fields need to be checked. This is
because every select type of field causes a check, even when that field is not used in any location rule. There is
really nothing at all that can be done about this since the only way to check to locations for each field group
is to do it with AJAX.

I'm going to look at adding an example of doing this with a specific field. Creating your own code for specific fields
will be much better for performance, and also would be much more versitile since you could not only use select type fields
but any type of field and make the location condtional on any type of a value.
