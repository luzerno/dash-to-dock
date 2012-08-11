# Dash to Dock Gnome Shell Extension
An extension for Gnome Shell that transforms the dash into an intellihide dock.

By default the Gnome Shell Dash is shown in the overview providing launchers for favourites and running aplications. This extension do move the dash out of the overview making it visible for easier launch of applications and faster switch between them without leaving the workspace view.

![screenshot](https://github.com/micheleg/dash-to-dock/raw/README/screenshots/master.jpg)

The dock supports **intellihide** and **autohide** mode. In addition the following customization options and features has been added to the default dash:

1. Customization of the maximum icon size.
2. Customizaton of the vertical position and alignment.
3. Option to show only favourites or running applications.
4. Switch workspace by scrolling over the dock.

Many options can be tweaked and tuned.

The extension supports **multi-monitor** configurations (see section below), *rtl-languages*, **accessibility** via Ctrl-Alt-Tab shortcut and is **theme-friendly**.

## Installation
### Gnome Shell 3.4
The easiest way to install and keep the extension updated is through the official Gnome shell extension site https://extensions.gnome.org/extension/307/dash-to-dock/. The installation process is straightfoward. The extension can then be enabled and disabled through the site or with *gnome-tweak-tool*.

### Gnome Shell 3.2
The version of extension uploaded to the extension site is outdated. An updated version with almost if not all the feautures of the master version can be downloaded from https://github.com/micheleg/dash-to-dock/downloads.

The extension can be installed by means of *gnome-tweak-tool* or direcly extractig the zip archive. Create a directory named <code>dashtodock@micxgx.gmail.com</code> inside <code>/home/user/.local/share/gnome-shell/extensions/</code> and extract the archive content there. Shell reload can be required <code>Alt+F2 r Enter</code>. The extension can be enabled with *gnome-tweak-tool* or with *dconf* by adding 'dashtodock@micxgx.gmail.com' to the <code>/org/gnome/shell/enabled-extensions</code> key.

### Install from source
The extension can be installed directly from source. Use the master branch for Gnome Shell 3.4 or the gnome-3.2 branch for Gnome Shell 3.2. A simple Makefile is included. Run 
<pre>make
make install
</pre>
to install the extension in your home directory. 

As an alternative the zip archive can be generated with 
<pre>
make
make zip-file
</pre>
Then follow the above instructions.

## Settings
### Gnome Shell 3.4 and above
The extension can be extensively configured by means of *gnome-shell-extension-prefs*. Click on the green icon on the extension site near the enable button or run <code>gnome-shell-extension-prefs</code> in a console. To open directly the Dash to Dock settings run 
<pre>
gnome-shell-extension-prefs dash-to-dock@micxgx.gmail.com
</pre>

### Gnome Shell 3.2
In Gnome Shell 3.2 the extension source code has to be modified in order to customize the extension settings. Settings are both in <code>intellihide.js</code> and in<code>dockedDash.js</code> inside the installation directory <code>/home/user/.local/share/gnome-shell/extensions/</code>. At the beginning of these files there is settings section with uppercase variables that can be easily set as preferred. They are mostly true/false variables and there are brief descriptions of the effect of each setting. Shell reload is required <code>Alt+F2 r Enter</code>.

#### Multi-monitor configuration
The extension support multi-monitor configurations. By default the dock is shown on the primary monitor that is the monitor where the overview is shown. The monitor where the extension is shown can be configured. If that monitor does not exist the dock keep being shown on the primary one. Moreover the dock position is automaticaly updated whenever a monitor is attached or removed so that you can set the dock to be shown on the external monitor and have the dock reapper on the laptop monitor when you remove the external one.

## Known Issues

## Change log

Version numbering follows the uploads to http://extensions.gnome.org

**Version 11 (22-07-2012)**
 * Allow to choose the monitor where the dock is shown.
 * Enable dash accessibility via ctrlAltTab.
 * Directly customize the dash background opacity.

**Version 10 (09-07-2012)**
 * Option to center the dock vertically.
 * Option to increase the maximum dock height.
 * Settings GUI overhaul.

**Version 9 (24-06-2012)**
 * Basic Bolt extensions support.
 * Bug fixing.

**Version 8 (23-06-2012)**
 * Gnome Shell 3.4 only release.
 * Greatly improve multimonitor support.
 * Improve intellihide efficiency.
 * Improve autohide.
 * Improve settings GUI.
 * Add swith workspace on scroll feature.
 * Option to control the maximum icon size.
 * Option to show favorites and/or running application icons.
 * Bug fixing.

**Version 7 (12-06-2012)**
 * Gnome Shell 3.2 only release, last version supporting 3.2.
 * Greatly improve multimonitor support.
 * Bug fixing.

**Version 6 (03-06-2012)**
 * Bug fixing.

**Version 5 (02-06-2012)**
 * Move settings to a gschema for Gnome Shell 3.4.
 * Add settings GUI form Gnome Shell 3.4.
 * Minor improvements.

**Version 4 (29-05-2012)**
 * Minor improvements.
 * Bug fixing.

**Version 3 (23-05-2012)**
 * Basic theme indipendece.
 * Intellihide/autohide settings.
 * Minor improvements.
 * Bug fixing .

**Version 2 (20-05-2012)**
* Inline timing settings.
* Bug fixing.

**Version 1 (12-05-2012)**
* Initial release.
* Basic intellihide functionality.