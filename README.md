Sublime Text 2 Ruby Tests
=========================

Overview
--------
Running:

  - ruby unit tests (all tests from file / single test)
  - cucumber tests (feature / scenario)
  - rspec (full spec, single spec)

Maciej Gajek & Grzegorz Smajdor (https://github.com/gs) project.

Installation
------------

Go to your Sublime Text 2 `Packages` directory

 - OS X: `~/Library/Application\ Support/Sublime\ Text\ 2/Packages`
 - Windows: `%APPDATA%/Sublime Text 2/Packages/`
 - Linux: `~/.Sublime\ Text\ 2/Packages/`

and clone the repository using the command below:

``` shell
git clone https://github.com/maltize/sublime-text-2-ruby-tests.git RubyTest
```

Settings
--------

You can specify different binary for each type of test to use.

Make a copy of `RubyTest.sublime-settings` file to `~/Library/Application Support/Sublime Text 2/Packages/User/` and make your changes.


Gary Bernhardt Split Mode
-------------------------

Makes split mode work like Gary Bernhardt's.  On his screencast "Destroy All Software" his vim configuration split moves depending on which file he's working on.

The default configuration will behave normally.  To enable the "Gary Bernhardt split mode" change 

    { "keys": ["super+ctrl+period"], 
      "command": "switch_between_code_and_test", 
      "args": {
        "split_view": true,
        "gary_bernhardt_split_mode": true },
      "context" : [{ 
        "key": "selector", 
        "operator": "equal", 
        "operand": "source.ruby", 
        "match_all": true }]
    }

A :30 video demo is available on YouTube:
http://www.youtube.com/watch?v=I_LZNorfCQ4&feature=youtu.be


Bundler support:
------------
First be sure that you have your copy of `RubyTest.sublime-settings` placed in User folder (refer to Settings above) and fill it  with below code:

    "erb_exec": "bundle exec erb",
    "ruby_unit_exec": "bundle exec ruby",
    "ruby_cucumber_exec": "bundle exec cucumber -f pretty",
    "ruby_rspec_exec": "bundle exec rspec",


Usage
-----

 - Run single ruby test: `Command-Shift-R`
 - Run all ruby tests from current file: `Command-Shift-T`
 - Run last ruby test(s): `Command-Shift-E`
 - Show test panel: `Command-Shift-X`
 - Check RB, ERB file syntax: `Alt-Shift-V`
 - Switching between code and test:
    - Single View: `Command-`.
    - Split View:  `Command+Ctrl+`.

Keys:
 'Command' (OSX)
 'Ctrl' (Linux / Windows)

 ![ruby_tests screenshot](https://github.com/maltize/sublime-text-2-ruby-tests/raw/master/ruby_tests.png)


Colors Issue:
------------
We have known colors issue. Please check [this thread](https://github.com/maltize/sublime-text-2-ruby-tests/issues/33#issuecomment-3553701) for temporary solution.

Note
----
Before reporting an issue be sure to :

  - Run Sublime Text 2 from [command line](http://www.sublimetext.com/docs/2/osx_command_line.html)

If this will not help provide to us debug informations using (CTRL + ` )

Please open an issue at https://github.com/maltize/sublime-text-2-ruby-tests if you discover a problem or would like to see a feature/change implemented.
