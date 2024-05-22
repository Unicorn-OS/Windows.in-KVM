# Display Resolution
sch: https://www.google.com/search?q=qxl+windows+resolution

Solution: https://community.frame.work/t/resolved-qemu-3-2-res-win11-guest/40851/2

>I managed to get it working just by installing the Virt-IO drivers for windows 11. @Viandant this managed to work for me without changing any scaling on the host. I was also able to use Virt-IO instead of QXL which allows me to enable 3D acceleration which is pretty great. For reference, I am using Wayland but im not sure if this makes a difference.
>
>I did add the following resolution line to the Virt-IO video section of the XML:
```
<video>
  <model type="virtio" heads="1" primary="yes">
    <acceleration accel3d="yes"/>
    <resolution x="2256" y="1504"/>
  </model>
  <address type="pci" domain="0x0000" bus="0x00" slot="0x01" function="0x0"/>
</video>
```
