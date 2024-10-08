
![FOSSx logo](/img/fossx.png)



This repository includes APKs specifically designed to test use cases of Frida for Android instrumentation.

### About Frida

Any program is made up of a sequential set of instructions, we can
observe it by opening up a program in a disassembler that is a list of
assembly instructions split into branches.
Frida can be used to hook into a program to get information about
how it behaves while it is running. Hooking into a program allows us
to intercept these instructions and make changes to how the program
works.

With Frida during the instrumentation process, not only we have de-
tailed information about the binary structure but also it is possible to
modify the execution flow of an application while it is running.


### Frida-tools

Frida-tools is a Python package that offers some CLI tools that can be
used for quick instrumentation.One of the two most important tools
that are present in the frida-tools package is the Frida command line
interface. 

Frida’s CLI is a very important tool because it kind of substitutes
the need for a control script and thus allows to quickly instrument a
binary or perform quick tests without the need of writing a full-fledged
instrumentation script.

-f switch allows to spawn a process given a path. When doing this, the
instrumented binary is spawned by Frida and the user is given access
to a command line. Frida will immediately continue the execution of
the application.

-I switch loads an instrumentation script. This is the most useful
switch because it allows to directly load an instrumentation script
in the process to be instrumented. When using this feature, Frida will
automatically detect changes to your script and inject the updated
script into the targeted application.

-U for USB instrumentation of devices connected via USB. Requires
a version synced frida-server running on the connected device.
In our testing scenarios, we have employed Frida version 16.1.10 for
conducting experiments and testing its functionalities.


### Resources

https://learnfrida.info/about_bininst/
https://codeshare.frida.re/