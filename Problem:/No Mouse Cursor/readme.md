# Problem: No Mouse Cursor
when: QXL & Discrete GPU
sch: https://www.google.com/search?q=qxl+windows+mouse+cursor Solution: https://superuser.com/questions/1278650/wacom-tablet-not-moving-cursor-under-kvm-windows-guest

# Solution:
## [No mouse with remote spice and Nvidia?](https://www.reddit.com/r/VFIO/comments/qiyn8z/no_mouse_with_remote_spice_and_nvidia/)

>SOLUTION
>The Nvidia driver seems to load after the QXL / Spice driver on boot, which consumes your mouse. You need to disable and re-enable it.

and
>Just thought I'd add in that there's a way to 'automate' this of sorts.You can disable and re-enable the device through powershell, and if you set this to run after login, it should get it done.
>
>`get-pnpdevice | where {$_.friendlyname -like "NVIDIA GeForce GTX 1080 Ti"}| disable-pnpdevice -Confirm:$false`
>
>`get-pnpdevice | where {$_.friendlyname -like "NVIDIA GeForce GTX 1080 Ti"}| enable-pnpdevice -Confirm:$false`

