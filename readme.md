# Cache Web Terminal
Web-based terminal application for InterSystems Cach&eacute; database. Access your database from the web, local network or even localhost.

### Ways to install terminal
<UL>
<LI>Just download XML from <a href="http://intersystems-ru.github.io/webterminal/#downloads">project page</a> and import it into %SYS namespace.</LI>
<LI>Use <a href="https://github.com/intersystems-ru/cache-tort-git">Cache Tort Git utility</a></LI>
<LI>Download an archive, unpack it and execute the following in %SYS namespace: <code>do $System.OBJ.ImportDir("UNPACK_FOLDER\", "*.xml", "ckbud", .err, 1)</code></LI>
</UL>

### About security and authorization

Terminal application is protected by using unique long identifier of CSP-session cookie now (v 0.9.9.5 and higher).
This means that logged user will have all roles and privileges that it has on server.
Unauthorized users will become "UnknownUser", so be patient.

### What's new?

#### v 0.9.9.5 (dev)
* Cache user privileges
* Authorization via CSP-sessions

#### v 0.9.9
* Russian translation
* Fixes in autocomplete, read, /tail, /sql
* Authorization from another namespace
* Other small fixes and improvements

#### v0.9.7

* New autocomplete rules: faster, better
* Wrong internal commands parsing (e.g. inside strings) fixed
* Huge data output crashes fixed

#### v0.9.6.8

* Added /tip command with detail tutorial of terminal functionality.
* Client-side commands parsing dialect changed and improved: check it in helpbox by typing "/tip" or "/tip all".
* It is possible now to define favorite commands/scenaries/programs.
* Fixed autocompletion for globals
* Added autocompletion for defines
* Fixed browser's autocomplete files caching
* "/autocomplete new" will regenerate file except of loading same file again
* /reset will reset autocomplete files on server
* Added /echo command
* Added /favourite command. Can be used as "<big code> /favorite {slot}" and then "/favorite {slot}"
* added /watch with same function as /tail
* /tail command without arguments will stop all watches
* Fixed Cache 2013.1
* Tested on Android 4.1, iOS 6

#### v0.9.5

* Added globals watching. Use /tail {filePath|globalName}
* Lots of fixes with client-side commands
* Highlighting comments
* Other small fixes including theme and autocompletion fixes
* Highlight output option
* iPad, Android optimization
* Testing and debugging

#### v0.9.1

* Added file watching. Type /watch {fullFilePath} to start watching for file changes. Type that again to stop
* Security improvement - server waits for authorization up to 3 seconds and then brakes connection
* Removed unnesesary debug variables which prevented normal application work
* Persistent settings (theme, options) saving
* Clean start option

#### v0.89

* Better error handling
* Autocompletion for local variables
* Autocompletion for globals
* Fixed wrong autocomplete priority for classes
* A bit speedy generation of autocomplete file (this isn't the limit)
* Cleaner theme declaration
* New monokai theme

#### v0.85

* Themes support added. Make your own terminal theme! Check first lines in js/application.js file.
* Storing history, terminal language and settings in local browser with new client-side commands /save /load and /reset
* Autocomplete priority - now you will get most frequently used variants first
* Added settings for automatical saving after session ends.
* Client-side commands won't get to history.
* Fixes for Firefox
* Other small fixes

### Usage
Point your browser to the following csp file: (http://[host]:[port]/csp/sys/webTerminal/index.csp) Type "/help" to get more information.
### Additional information
Visit [project page](http://intersystems-ru.github.io/webterminal) for extra information.
### Description
<table>
	<tr>
		<td class="hint">Feature</td>
		<td class="hint">Description</td>
	</tr>
	<tr>
		<td class="info">WebSocket protocol</td>
		<td>Provides stable and solid client-server connection.</td>
	</tr>
	<tr>
		<td class="info">Autocompletion</td>
		<td>While entering commands, notice hints appearing in gray font. Hit &lt;TAB&gt; to extend your current input with suggested variant. If there is more than one hint available, you can choose best variant by pressing &lt;CTRL&gt; or &lt;ALT&gt;.</td>
	</tr>
	<tr>
		<td class="info">File/Globals watching</td>
		<td>Monitor any changes in globals or files using /tail command</td>
	</tr>
	<tr>
		<td class="info">Syntax highlighting</td>
		<td>Browser can divide code into logical blocks and style them according to syntax.css style definitions.</td>
	</tr>
	<tr>
		<td class="info">Appearance</td>
		<td>Change the look of web-terminal as you wish, and even make you own theme!</td>
	</tr>
	<tr>
		<td class="info">History</td>
		<td>Browser remembers command history, just use arrow keys to walk through it.</td>
	</tr>
	<tr>
		<td class="info">Copy/Paste</td>
		<td>Select and copy text you need. Paste any combination of symbols into terminal input.</td>
	</tr>
	<tr>
		<td class="info">Security</td>
		<td>Access to WebSocket is granted only if client has a hash generated by csp page. This makes it impossible to bruteforce opened WebSocket.</td>	</tr>
	<tr>
		<td class="info">Accessibility</td>
		<td>Copy your current URL and send to anybody you want. Terminal is session-independent, so you can use your own variables without thinking about other users.</td>
	</tr>
	<tr>
		<td class="info">And even more...</td>
		<td>New features <s>and bugs</s> are coming!</td>
	</tr>
</table>
