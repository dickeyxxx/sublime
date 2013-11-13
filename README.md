@dickeyxxx Sublime 2 Config
===========================

This is my customized Sublime Text 2 config.

Requirements
------------

Install [Sublime Text 2](http://www.sublimetext.com/).

Install [Package Control](http://wbond.net/sublime_packages/package_control) by opening `View > Show Console` and pasting this:

```
import urllib2,os; pf='Package Control.sublime-package'; ipp = sublime.installed_packages_path(); os.makedirs( ipp ) if not os.path.exists(ipp) else None; urllib2.install_opener( urllib2.build_opener( urllib2.ProxyHandler( ))); open( os.path.join( ipp, pf), 'wb' ).write( urllib2.urlopen( 'http://sublime.wbond.net/' +pf.replace( ' ','%20' )).read()); print( 'Please restart Sublime Text to finish installation')
```

Then restart Sublime.

Installation
------------

Go to your Sublime Text 2 Packages directory:

```bash
cd ~/Library/Application\ Support/Sublime\ Text\ 2/Packages/
```

Clone the settings repository using the command below:

```bash
$ rm -rf User
$ git clone https://github.com/dickeyxxx/Sublime-Text-2-User-Settings.git User
```

Notes
-----

To get the `subl` command:

```bash
$ ln -s "/Applications/Sublime Text 2.app/Contents/SharedSupport/bin/subl" /usr/local/bin/subl
```

To make Sublime your default editor, run this command:

```bash
$ echo 'export EDITOR='subl -w' >> ~/.bash_profile
```

I use the `vintage` plugin that makes Sublime act like vim (you may not want this). To disable, add this to your User Preferences:

```json
"ignored_packages": ["Vintage"]
```