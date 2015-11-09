Anytoggle
=========

Toggle any program with a single shortcut / command

Anytoggle starts a program if it doesn't run yet. And if it is already running,
it will toggle the window's visibility. In a way, you can use it as a poor man's
Guake/Yakauke etc:

    anytoggle --title MYOWNQUAKETERMINAL --start 'sakura -t MYOWNQUAKETERMINAL'

Every time you run this command, it will look for a window with
MYOWNQUAKETERMINAL as a name. If it is found, it is activated (brought to the
current desktop, and raised). If not, the command denoted with the --start parameter is executed.

Oh, and if the program is currently active, it's window is hidden.

The whole thing is thought to be used with your window manager / desktop
environment's shortcut mechanism. I for one have put the following into my
openbox RC file:

    <keybind key="Pause">
        <action name="Execute">
            <execute>/usr/bin/anytoggle --title IRC --start 'sakura -t IRC'</execute>
        </action>
    </keybind>
