## v0.9.2 (16.1.2015) ##

  * New Features
    * configurable commands on ON, OFF and per sampling interval
    * command sequencing using the semicolon as delimiter
    * adds MODBUS read, wcoil, wcoils commands and last result substitution variable accessible via the underline character
    * adds [HukyForum.com](http://www.hukyforum.com/index.php) image export
  * Bug Fixes
    * fixes color dialog for extra devices on OS X
    * fixes a potential crasher caused by x-axis realignment during sampling
    * fixes communication issues with Phidgets especially in remote mode via an SBC
    * fixes WebLCD startup issues on slow Windows machines
    * fixes MODBUS over UDP/TCP IPv6 issues on Windows

## v0.9.1 (3.1.2015) ##

  * New Features
    * adds QR code for WebLCD URL
    * adds keyboard short cut to retrieve readings from a serial scale (press ENTER in roast properties weight-in/out fields or volume calculator field)
    * adds support for the acaia BT coffee scale
    * adds serial scale support to Volume Calculator
    * adds tare support to Volume Calculator
  * Changes
    * changes x-axis minor ticks to one minute distance
    * Python updated to v2.7.9
    * Italian translations update
  * Bug Fixes
    * fixes Arduino/TC4 temperature units
    * fixes button value restoring on palette load
    * fixes Volume Calculater unit conversion


## v0.9.0 (17.11.2014) ##

  * New Features
    * adds MODBUS ASCII/TCP/UDP support (via pymodbus)
    * adds Yocto thermocouple and PT100 support
    * adds Phidget 1045 IR support
    * adds support for Phidgets 1046 Wheatstone Bridge wiring variant
    * extended Phidgets configurations (adds async support, data rates and change triggers)
    * adds program\_34 and program\_56 device to read extra channels from external program
    * adds DUMMY device that returns always 0 to allow mapping of extra channels to the main device (ET/BT)
    * adds "wcoils" to write MODBUS command "Write Multiple Coils" (function 15)
    * extended Italien translations
    * adds Polish translations
    * logs active non-zero slider values at CHARGE
    * adds coarse quantifiers 0-10, 10 steps instead of 100 as for standard quantifiers
    * Phidget 1048 sets ambient temperature (in roast dialog) automatically on DROP
    * adds quick custom event keybord shortcuts (keys q-w-e-r followed by 3 digits)
    * file from which alarms were loaded is now displayed in the alarms dialog
    * extends phases lcds by Rao's style ratios and BT deltas
    * adds MET calculation (maximum ET between TP and DROP)
    * adds moisture of roasted beans to roast properties
    * background title as subtitle
    * adds flag to align of background profiles also wrt. FCs
    * adds button action to set digital outputs on Phidgets IO
    * adds BT/ET rate-of-rise to the designer
    * adds "Delta Span" setting
    * adds "Call Program" action to sliders
    * LargeLCDs and WebLCDs
    * adds 2nd characteristics line on right click
    * adds time axis lock mode
    * adds a volume calculator
    * adds moisture loss and organic loss calculation
    * second set of phases definitions (now one for Espresso and one for Filter roasts)
    * adds configuration of Arduino/TC4 filter settings
    * container tare setup
  * Changes
    * recent file menu size extended from 10 to 20 entries
    * missing files are removed from recent file menu
    * automatic saved files are added to the recent files menu
    * updated build setup on Windows and Mac OS X
    * quantifier range extended from [-999,999] to [-99999,99999]
    * removes leading zeros from time annotations
    * faster OFF
    * moved Phidgets configurations to extra tab
    * precision of times and temperatures in stored profiles extended by another digit
    * alarm dialogs auto close after 10sec
  * Bug Fixes
    * fixes autosafe failure on invalid filenames
    * allow to hide HUD button and Control button in ArduinoTC4 mode
    * all serial ports and other connections are closed on OFF
    * x-Axis min limit can now be set to 00:00
    * fixed palette switching using keyboard shortcuts
    * native color dialog on Mac OS X blocked other dialogs and menu actions
    * call-program action fixed
    * mouse cross lines in deltaBT/ET mode fixed
    * fixed designer resize redraw issue
    * fixed the Fuji PXR SetRS
    * phases were updated on profile load despite the Auto Adjust phases not being ticked
    * CSV roundtrip on Windows
    * missing reset before import added
    * settings are stored on closing Artisan by closing its main window
    * fixed quantifier application

## v0.8.0 (25.05.2014) ##

  * New Features
    * adds Mastech MS6514 support
    * adds Phidget IO support (eg. 1018 or SBC)
    * adds Phidget remote support (eg. via SBC)
    * adds Arduino TC4 PID support
  * Changes
    * increased Arduino TC4 default serial baud rate from 19200 to 115200 to match the TC4 Firmware aArtisan v3.00
    * saves autosave path and Volume/Weight/Density units to app settings
    * roast profile data table and events value display respect decimal places settings
    * improved extra device handling on profile loading
    * simplified statistics line
    * updates libraries (Qt, PyQt, numpy, scipy)
    * do not load alarms from background profiles
  * Bug Fixes
    * fixes keyboard mode on reset
    * fixes multiple event button action
    * fixes mixup of alarm table introduced in 0.7.5

## v0.7.5 (06.04.2014) ##

  * New Features
    * adds Phidgets 1048 probe type configuration
    * adds event quantifiers
    * adds CM correlation measure between fore- and background profile to statistics bar
    * adds symbolic variables for background temperatures for symbolic assignments
    * adds xy scale toggle via key d
    * adds modbus temperature mode per channel
    * adds Modbus/Fuji merger
  * Changes
    * increased resolution of temperatures in profiles to two digits
    * updated Modbus lib (slightly faster)
  * Bug Fixes
    * improved serial communication
    * fixed extra event manual entry to allow digits
    * adds security patch
    * fixed background profile color selection
    * font fix for OS X 10.9


## v0.7.4 (13.01.2014) ##

  * Bug Fixes
    * fixes ETBT swap functionality

## v0.7.3 (12.01.2014) ##

  * New Features
    * adds oversampling
    * adds support for floats to the Modbus write command
  * Changes
    * improved curve and RoR smoothing
    * improved autoCharge/autoDrop recognizer
    * updated Phidget library

## v0.7.2 (19.12.2013) ##

  * Changes
    * beep after an alarm trigger if sound is on and beep flag is set
    * autosave with empty prefix takes roast name as prefix if available
    * external program path added to program settings
  * Bug Fixes
    * fixed always active min/max filter
    * spike filter improvements
    * fixes time axis labels on CHARGE
    * fixed alarm trigger for button 1
    * improved autoCHARGE and autoDROP recognizers
    * fixes minieditor event type handling
    * fixes and improvements to [RoastLogger](http://homepage.ntlworld.com/green_bean/coffee/roastlogger/roastlogger.htm) import
    * makes the extra serial ports widget editable


## v0.7.1 (02.12.2013) ##

  * Bug Fixes
    * fixes lockup on extra device use
    * fixes redraw artifact on axis changes
    * fixes minieditor navigation
    * fixes early autoDRY and autoFCs
    * fixes extra lines drawing

## v0.7.0 (30.11.2013) ##

  * New Features
    * adds support for the [Phidget 1046 4-Input PT100/RTD  Bridge](http://www.phidgets.com/products.php?product_id=1046_0) and for the [Phidget 1048 4-Input Temperature Sensor J/K/E/T-Type](http://www.phidgets.com/products.php?product_id=1048) devices
    * adds TP event marks (show on graph and in the message log)
    * adds flag in events dialog to control the display of the TP mark
    * adds autoDRY and autoFCs to phases dialog
    * adds phase LCDs (TP, DRY, FCs) estimating time to the event and counting time after the event
    * adds flag in phases dialog to deactivate phases LCDs
    * keeps a link to the loaded background file on saving a profile and automatically re-loads the background with the actual profile
    * adds a new graph style using xkcd, path effects and the Humor or Comic font
    * alarms
      * option load/save alarms along (background-) profiles
      * adds negative alarm guards "But not"
      * adds insert alarm button
      * adds new alarm actions to trigger default event actions like START, FCs,..
      * triggered alarms hold a gray background in the alarms dialog
      * imports alarms from [RoastLogger](http://homepage.ntlworld.com/green_bean/coffee/roastlogger/roastlogger.htm) profiles (thanks to Miroslav)
    * allows ETBTa and RoR statistics to be displayed together
    * adds support for the [Tonino roast color meter](http://my-tonino.com)
    * the last used extra event button is marked
    * adds extra device data to Roast Properties data table
    * adds "cool end" event to the event popup menu on right mouse click on the BT
    * adds "Fuji SV" as second channel to the +Fuji DUTY %
    * adds load/save and read/write all actions to Fuji control
    * adds keyboard control for sliders
    * adds an option to remove digits from temperature LCDs (extras dialog)
    * adds Hebrew localization
  * Changes
    * curve smoothing settings sensitivity has been doubled (for some internal reasons). So a value of 6 on Artisan v0.6 should be adjusted to 3 to have roughly the same effect.
    * autosave now takes the roast name from the roast properties and autosaves on OFF. Further, the date is now written as prefix
    * preserves autosave ON/OFF state over app restarts
    * x/y mouse pointer coordinate display now always displays temperatures and not temperature deltas if the RoR axis is active
    * reorganized tabs in Extras dialog
    * removes axis labels during recording
    * alarms guarded by TP event are now active beyond the DRY event
    * removed scan for ports button
    * legend only shows extra event types that are in use
    * alarm dialog edits directly the active alarm table with the consequence that alarms are not retriggered if
    * alarms are edited during roasting
    * right axis removed if DeltaET/BT is not active
    * extra courve LCDs are now of the same size as the ET/BT LCDs
    * updated underlying libs (Python, Qt, matplotlib)
  * Bug Fixes
    * fixes issues with the "Drop Spikes" filter
    * fixes "import profile into designer" action
    * fixes default directory in wheelgraph open file dialog
    * various fixes to the rendering of background profile annotations
    * fixes an issue that allowed alarms to be trigger several times
    * Windows font fixes
    * fixed events-by value redraw if minieditor is open
    * fixed a conflict between manual device ENTER key action and manual temperature input dialog
    * improved reliability of serial and modbus commands
    * fixes issue with Roast Reports on Windows
    * several fixes to alarm system
    * fixes the [RoastLogger](http://homepage.ntlworld.com/green_bean/coffee/roastlogger/roastlogger.htm) import of latin1 encoded files
    * PID LCD visibility
    * scan for ports on Linux
    * better error handling on exporting data
    * improved sample time accuracy
    * fixes wrong segment 4 soak time reported by "Read RS values"
    * updates translations (JP, NL)

## v0.6.0 (14.6.2013) ##

  * Events
    * adds COOL event recording the time the beans were cooled down
    * adds event sliders e.g. to control the Hottop heater and fan via the HT Roaster Interface
    * adds substitution of '{}' in event button/slider actions by button value
    * adds Modbus and DTA send command support attached to button events
    * adds ordering of events in events tab of Roast Properties dialog
    * event value range extended from [0-10] to [0-100]
    * allows events like FCs, FCe,.. (but for CHARGE) to be removed by inserting 0:00 as event time
  * Alarms
    * adds alarm chains via alarms guarded by other alarms added
    * adds alarms on all logged temperature curves incl. deltaET/deltaBT
    * adds alarms on rising and falling temperatures
    * adds SC\_END, COOL and TP to the FROM list of alarms
    * adds an empty alarm action (None)
    * adds emtpty alarm from-time (START)
    * adds COOL event trigger as special case (via button #0)
    * adds slider change actions
    * adds time-based alarms triggered at the given seconds after the specified event like TP, FCs,..
    * adds save/load action to alarm table
  * Curves
    * adds ET/BT swap configuration
    * adds ambient temperature routing added
    * adds background deltaET/deltaBT
    * adds spike filter and smoothing
    * adds smoothing of all curves incl. background on load/redraw (not only DeltaET/DeltaBT)
    * improved and faster DeltaET/BT smoothing (via numpy)
    * adds customization of line and marker styles via the Figure Options menu (green flag button)
  * Supported Devices
    * adds 4 channel MODBUS RTU device support
    * adds improved Delta DTA/DTB support
    * adds support for digital scales from KERN
    * adds support for Amprobe TMD-56
  * UI
    * improved main window widget layout
    * improved dialog layouts
    * adds colorized LCDs using curve color
    * forces even x-axis ticks
    * adds dpi resolution and appearance application settings
    * adds full-screen support
    * adds new and improved localizations (Arabic, German, Greek, Spanish, French, Japanese, Norwegian, Portuguese, Turkish, Dutch, and Italian)
    * adds monitoring-only mode reporting readings on LCDs without recording. To start recording press START
    * adds customization of visibility of LCDs, curves, and default event buttons
    * improved label positioning on graphs
    * improved HTML Report (now called Roast Report)
    * adds automatic table columns resize to content and to dialog size
    * adds long cool phase warning (red time LCD)
    * adds BTETarea statistics per phase
    * adds user-definable default button actions
    * adds customization of default button visibility
    * adds optional hiding of ET/BT curves and ET/BT/DeltaET/BT LCDs
    * adds line- and marker styles set via the "GreenFlag" menu to application settings
    * fixed figure options dialog (green flag menu)
    * adds right-click popup on BT curve to change event time
  * File Handling
    * changed default directory on Mac from ~/Library to ~/Documents
    * changed file extension of profiles from .txt to .alog
    * adds load-by-double-click (Mac OS X only)
    * adds JSON import/export
    * adds RoastLogger import/export
    * adds PDF/SVG vector graph export
  * Packaging
    * removes support for PPC processors on the OS X platform
    * adds Linux binary builds (32bit and 64bit)
    * adds Windows installer
    * adds new app and file icons
    * upgrades underlying libs (Python, Qt, PyQt, numpy, scipy, matplotlib)
  * Others
    * adds Python 3 support
    * adds auto align background on CHARGE/autoCharge
    * improved localization support and unicode character handling
    * adds a CUSTOM cup profile that is stored in the application settings
    * adds computation of the area between the BT and ET curves (ETBTa)
    * adds extended roast characteristics/statistics (incl. ET/BT area abbreviated as ETBTa)
    * adds roast color and flags to specify roast defects
    * adds polyfits
    * bug fixes


---

## v0.5.6 (8.11.2012) ##

  * based on [r787](https://code.google.com/p/artisan/source/detail?r=787) (with modbus support removed)
  * added support for Voltcraft K201 and fixed CENTER 301
  * bug fixes


---

## v0.5.5 (28.9.2011) ##

  * fixes ArdruinoTC4 extra devices
  * fixed autoDrop recognition
  * fixes serial settings for extra devices


---

## v0.5.4 (28.8.2011) ##

  * adds events by value
  * adds custom event button palettes
  * adds virtual device from plot
  * adds K204 CSV import
  * improves Designer
  * improves Statistics
  * improves Help dialogs
  * improves relative times
  * bug fixes


---

## v0.5.3 (30.7.2011) ##
  * improves performance of push buttons
  * adds device external-program
  * adds trouble shooting serial log
  * fixes Linux Ubuntu and other bugs


---

## v0.5.2 (23.7.2011) ##

  * added Delta DTA PID support
  * added automatic CHARGE/DROP event detection
  * added separate RoR axis
  * added cross lines locator
  * smaller Mac OS builds with faster startup
  * optimized legend and statistics layout
  * improved Wheel Graph editor
  * performance improvements
  * bug fixes


---

## v0.5.1 (18.6.2011) ##

  * bug fixes


---

## v0.5.0 (10.6.2011) ##

  * support for Mac OS X 10.4 and PPC added
  * added more translations
  * added wheel graph editor
  * added custom event-control buttons
  * added Omega HHM28 multimeter device support
  * added support for devices with 4 thermocouples
  * added PID duty cycle
  * added math plotter in Extras
  * added run-time multiple device compatibility and symbolic expressions support
  * improved configuration of Axes
  * improved configuration of PID
  * improved Arduino code/configuration
  * improved cupping graphs
  * improved performance/responsiveness in multi-core CPUs
  * bug fixes


---

## v0.5.0b2 (04.6.2011) ##

  * improved cupping graphs
  * improved performance in multi-core CPUs
  * bug fixes


---

## v0.5.0b1 (28.5.2011) ##

  * support for Mac OS X 10.4 and PPC added
  * added more translations
  * added wheel graph editor
  * added custom event-control buttons
  * added Omega HHM28 multimeter device support
  * added support for devices with 4 thermocouples
  * added PID duty cycle
  * added math plotter in Extras
  * added run-time multiple device compatibility and symbolic expressions support
  * improved configuration of Axes
  * improved configuration of PID
  * improved Arduino code
  * bug fixes


---

## v0.4.1 (13.4.2011) ##

  * import of CSV is not limited anymore to filenames with "csv" extension
  * improved VA18B support
  * Windows binary includes the language translations that were missing in v0.4.0


---

## v0.4.0 (10.4.2011) ##

  * improved CSV import/export
  * K202 CSV support added
  * adds localization support
  * adds german, french, spanish, swedish, italian menu translations
  * fixed cut-copy-paste on Mac and added cut-copy-paste menu
  * LCD color configuration
  * replay of events via background dialog
  * relative times are used everywhere
  * adds profile designer
  * adds alarms
  * more robust Arduino/TC4 communication
  * bug fixes


---

## v0.3.4 (28.02.2011) ##

  * adds Arduino/TC4 device support
  * adds TE VA18b device support
  * improved Fuji PXR/PXG support
  * support for file paths with accent characters
  * main window layout improvements
  * improved events visualization and capacity
  * improved roasting properties dialog
  * statistic characteristic line as y-label to ensure visibility if axis limits are changed
  * duplicate recent file names show containing directory
  * remembers user selected profile path
  * added DeltaET/DeltaBT filter to make those delta curves more useful
  * adds volume and bean probe density
  * adds new command to start/restart roasts
  * bug fixes


---

## v0.3.3 (13.02.2011) ##

  * fixed typo in htmlReport
  * fixed phases automatic adjusting mechanism
  * serial communication improvements
  * added support for Fuji PXR5/PXG5
  * added NONE device
  * added keyboard shortcuts for events and sound feedback
  * initial Linux binary release
  * added axis settings to application preferences


---

## v0.3.2 (31.01.2011) ##

  * fixed Center 309 communication
  * fixed serial device scan on Linux
  * added support for Omega HH309
  * added open recent, save and (CSV) export menus
  * added DRY END Button
  * added sync of mid phase with the DRY END and FCs events
  * added custom event types
  * added events type mini editor widget
  * added math tab in extras dialog
  * added ambient temperature to roast properties
  * extended projection mode
  * updated several software components
  * improved statistic bar positioning
  * new mailing lists for users and developers established


---

## v0.3.1 (12.01.2011) ##

  * fixed issue on loading the user's application preferences


---

## v0.3.0 (11.01.2011) ##

  * fixed occasional ET/BT swap
  * fixed issues wrt. accent characters
  * added 10.5.x support for Intel-only
  * new file format to store profiles
  * added configurable min/max values for x/y axis
  * added alignment of background profile wrt. CHARGE during roast
  * added DeltaBT/DeltaET flags
  * added "green Flag" button on Windows
  * reorganized dialogs and menus
  * added new HUD mode
  * smaller changes and additions


---

## v0.2.1 (02.01.2011) ##

  * bug fixes


---

## v0.2.0 (31.12.2010) ##

  * added support for
    * CENTER 300, 301, 302, 303, 304, 305, 306
    * VOLTCRAFT K202, K204, 300K, 302KJ
    * EXTECH 421509
  * bug fixes


---

## v0.1.0 (20.12.2010) ##
  * Initial release

---
