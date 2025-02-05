# Objective-C: Subtle `self` Usage and `performSelector` Delay Issues

This repository demonstrates two uncommon but potentially problematic scenarios in Objective-C programming:

1. **Incorrect `self` Usage During Initialization:**  Improper handling of `self` within initialization methods (`-init`, `-initWith...`) can lead to crashes or unexpected behavior if `self` isn't fully initialized before accessing its properties.
2. **`performSelector:withObject:afterDelay:` Issues:** Using `performSelector` with a delay can cause problems if the object on which the selector is called gets deallocated before the delay is over, resulting in crashes.

The `bug.m` file shows the problematic code, while `bugSolution.m` presents the corrected version.