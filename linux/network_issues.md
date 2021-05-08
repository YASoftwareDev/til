# Ethernet "cable unplugged" after waking up from suspension/starting system

https://forums.linuxmint.com/viewtopic.php?t=284338

TL&DR:

```
sudo rmmod r8169 && sudo modprobe r8169 && sudo systemctl restart network-manager.service
```

explanation:

```
inxi -Fxz
```

or (network section)

```
lspci -k
```

shows network driver. Removing/restoring, restarting service helps (exactly the same as with bluetooth dongle).
