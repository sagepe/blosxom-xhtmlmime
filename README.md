# Blosxom plugin - xhtmlmime

This is an old [Blosxom](http://blosxom.sourceforge.net/) plugin written back in 2005. Notes below are from the in-line POD.

## Description
This plugin is designed to return a `Content-Type` HTTP header of `application/xhtml+xml` to user agents that indicate they prefer it to `text/html` in their `Accept` HTTP header.

The highly useful `CGI.pm` does all the work, even down to interpreting `q` values.

You can force the plugin to use `application/xhtml+xml` by specifying a URL parameter of `mime=xhtml`.  Setting `mime` to anything else will cause the plugin to use `text/html`.

## Configuration
There are two configurable variables:

Set `$flavours` to a list of the flavours that you want the plugin to act upon.  If this variable is empty, the plugin will quietly exit without doing anything.  Separate each flavour using the vertical bar character, `|`.  For example: `my $flavours = 'htm|html';`

Set `$charset` to the encoding used on your website.  The default is `utf-8`, but other common English-language codes are `iso-8859-1` or `windows-1251`.

## See Also
[Blosxom and application/xhtml+xml](http://sgp.me.uk/2005/06/06/xhtml-mime-plugin).

I am aware that another similar plugin named `xhtml` was once written.  I was unable to locate a copy after a cursory bit of googling, so I wrote this one.  I would be surprised if there were any substantial differences between the two.
