# ![uRadMonitor BitBar]

This script allow you to show current radiation level on your Mac OS X Menu Bar

It grab value of your uRad device (http://www.uradmonitor.com/products/), process it (CPM to uSv/h conversion) and show it.
A color scale is used, with same color than uRad map (http://www.uradmonitor.com/)

It use BitBar (by [Mat Ryer - @matryer](https://twitter.com/matryer)) lets you put the output from any script/program in your Mac OS X Menu Bar.

  * [Download latest BitBar release](https://github.com/matryer/bitbar/releases/latest) - requires Mac OS X Lion or newer (>= 10.7)
  * [Visit the app homepage at https://getbitbar.com](https://getbitbar.com) to install plugin

## Get started

[Use uradmonitor-bitbar plugin](https://github.com/martinlbb/uradmonitor-bitbar/blob/master/uRadMonitor.30s.sh). Copy  it to a blank directory on your computer. That directory will be the BitBar [plugin directory].

[Modify IP in the uradmonitor-bitbar plugin]. Using a text editor (vi, BBEdit, ...), edit the [uradmonitor-bitbar] plugin. Find the IP line, and modify to your needs.

[Get the latest version of BitBar](https://github.com/matryer/bitbar/releases). Copy it to your Applications folder and run it - it will ask you to select a plugins folder, do so. Browse to the directory where you already downloaded [uradmonitor-bitbar] plugin.

[It's done !] You current radiation level will be showned!

## Modify it, configure it

### Show another value
You can show another value instead of default one. Just uncomment selected printf at the end of file.
If more than one value is enabled, BitBar will show all in a menu.

### Configure the refresh time

The refresh time is in the filename of the plugin, following this format:

    {name}.{time}.{ext}

  * `name` - The name of the file
  * `time` - The refresh rate (see below)
  * `ext` - The file extension

For example:

  * `date.1m.sh` would refresh every minute.

Most plugins will come with a default, but you can change it to anything you like:

  * 10s - ten seconds
  * 1m - one minute
  * 2h - two hours
  * 1d - a day

### Ensure you have execution rights

Ensure the plugin is executable by running `chmod +x plugin.sh`.

### Using symlinks

Because Git will ignore everything in `Plugins/Enabled`, you can use it to maintain your own plugins directory while still benefitting from tracking (upstream) changes.

#### Resetting Plugin Directory

In case you made the mistake of choosing a directory with thousands of files as the plugin directory and BitBar getting stuck forever, do this from terminal to reset it:

`defaults delete com.matryer.BitBar`



## Plugin API
  https://github.com/matryer/bitbar#writing-plugins
