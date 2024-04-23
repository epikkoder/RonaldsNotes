In Visual Studio, pressing `F10` to debug stops to the very first line of code that runs.

Pressing `Ctrl + F10` does "Run to cursor", where the app runs and stops at the line of code where you did the command.

You can drag the arrow up the code where it's currently stopped to run the previous code. (You need to be careful when doing this, as "this may have unintended consequences.")

## Common Debugging Traps
- Don't guess or try random things in code
- Don't assume the problem is trivial
- Don't code for "special cases"
- Don't debug by superstition

The "Autos" window shows variables around a breakpoint.
> [!info] You can track an object in the "Autos" windows by right-clicking on it and selecting "Make Object ID", so even if it goes out of scope, you can still see its properties. This works for reference types. It automatically gets added in the "Locals" window.

The "Locals" window shows variables defined in the local scope.

You can pin properties of an object to show on the higher-level overview.
![[pin_to_overview.gif]]

You can also pin variables to always show their current value.
![[pin_variables_to_overview.gif]]

The "Immediate" window is where you can run code and change a variable's value while debugging.
![[immediate_window.gif]]