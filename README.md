# Automatic Memrise Bot (Pynput version)

A program that automatically does a Memrise learning course for you. It will get you the target you need swiftly and efficiently.

---

**Important message** - use this ethically. Memrise is there to teach you a new language - whether it be for a subject or a hobby, at the end of the day, the only person you're cheating is _yourself_.

---

<b>Note:</b> The program does not work with the new, beta redesign for Memrise, and so you should definetly make sure that in `Settings --> Learning` ([memrise.com/learning-settings](https://app.memrise.com/learning-settings)) that all the options are toggled OFF.

Also, when you click on `Settings`, scroll down to <b>The new Memrise experience (Beta)</b>, and make sure that the checkbox is <b>unchecked.</b>
Do the same for <b>Memrise Labs (Alpha)
</b>, so that both checkboxes are <b>unchecked</b>.

Note that this program only works when learning new words, because, quite literally, the program will _learn_ the words itself. It cannot do reviews because it does not have the data to do so.

## About the Project (important usage info as well):

-   Clone the repository: `git clone https://github.com/mjsandagi/memrise-auto-bot.git` or download the zip folder (unzip it).
-   Make sure you have Python installed - [python.org/downloads](https://www.python.org/downloads/). Add the necessary commands to PATH.
-   Open Windows Powershell (or your preferred terminal) and install the non-native python library "pynput" via `C:/memrise-auto-bot> pip install pynput`
-   To run the program, open a terminal in the directory "memrise-auto-bot" and run the python file - `C:/MemriseAutoBot> python clavorum.py`
-   Pynput is used to take control of the Keyboard and Mouse, hence enabling the program to automatically complete the course.
-   The program will ask you to enter a set number of points that you wish to achieve. It will then give you ~15 seconds to close all the tabs.
-   <b>IMPORTANT</b>: Once the project has been set to run, you need to Alt-Tab to the web browser. Then, open <b>txt.txt</b> in <b>notepad</b>, and Alt-Tab between txt.txt (which should be open in Notepad) and the web browser. After doing this, Alt-Tab to the browser and leave it alone. The program shall automatically start. <br> <b>If what I said was complicated, simply click on the Notepad file and then click onto the browser with the Memrise course open.</b>
-   Clear the txt.txt file (as well as the translation file created) every time you start a new session.

### Complicated stuff about the new Memrise Beta & Alpha:

-   The newer Memrise redesigns have the CSS `user-select` property defined as `none`, which means that the program cannot copy and paste some of the text on the screen.
-   As a workaround, you will manually need to open the developer console (ctrl-shift-i), and add the following CSS property in (This needs to be done every session):

```
div {
    user-select: text;
}
```

-   As of commit 103ee10 you can:
-   Change `if len(lst[-i]) > 2:` on line 50 to a `if len(lst[-i]) > 3:`. The program will then function normally.

### License

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
