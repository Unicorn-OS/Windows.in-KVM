sch: https://www.google.com/search?q=qxl+mouse+cursor+missing https://www.google.com/search?q=qxl+mouse+pointer+missing https://www.google.com/search?q=kvm+xml+show-cursor

# Discuss:
- https://superuser.com/questions/1546702/qemu-no-visible-cursor-when-using-qxl-or-virtio
- https://www.reddit.com/r/kvm/comments/16oiby0/qemukvm_to_always_show_guest_cursor/
- https://superuser.com/questions/1828045/prevent-mouse-from-being-hidden-in-ubuntu-when-running-as-kvm-qemu-guest

# doc:
https://libvirt.org/kbase/qemu-passthrough-security.html

# Solution:
https://askubuntu.com/questions/730891/how-can-i-get-a-mouse-cursor-in-qemu

qemu:
```
-display default,show-cursor=on
```

xml:
```
<domain>
...
  <commandline xmlns="http://libvirt.org/schemas/domain/qemu/1.0">
    <arg value='-display'/>
    <arg value='default,show-cursor=on'/>
  </commandline>
</domain>
```
