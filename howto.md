# How to

- unpack tar from dir: ./sources/boot.wim&install.esd
```
cat 'boot.wim&install.esd.tar.0'* | tar xvf - -C ../
```

- install mkisofs
```
sudo apt install genisoimage
```
- create iso
```
mkisofs -o Tiny10.iso -b bootmgr -no-emul-boot -boot-load-size 8 -boot-info-table -c boot.catalog -J -R -hide-rr-moved -V "Tiny10_Custom_Install" .
```

