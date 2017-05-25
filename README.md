# ACF Custom Field Location Rules

Set ACF field group location based on select, checkbox, radio and true/false fields in other field groups.

***Please see my notes about issues with this plugin***

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

***Overall, using this plugin is probably a very bad idea for any site, especially sites that has a large number of field groups or
a large numbers of choice fields. This plugin will put a heavy burden on page loading when many fields need to be checked. This is
because every choice type of field causes a check, even when that field is not used in any location rule. There is
really nothing at all that can be done about this since the only way to check for locations for each field group
is to do it with AJAX. Your purposes would probably be better served by using this as an example and creating custom location rules
for specific fields that you wish to use for determining the locations of field groups.***

I'm going to look at adding an example of doing this with a specific field if I can find the time to do so.
Creating your own code for specific fields will be much better for performance, and also would be much more versitile 
since you could not only use choice type fields but any type of field and make the location condtional on any type of a value.
