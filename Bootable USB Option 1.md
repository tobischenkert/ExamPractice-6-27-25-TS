# __How to create a boot-able USB for Windows:__ 

__How to create a boot-able USB for Windows:__ 

Minimum size of the USB Drive: 8GB but 16GB+ is recommended. 


Option 1: Download and install Rufus from the Internet -> Download and install the preferred Windows ISO file from Microsoft.  [The Link for Windows 11](https://www.microsoft.com/en-us/software-download/windows11) -> Plug in your USB -> Choose the USB in Rufus -> Select the ISO FIle -> Choose MBR or GPT as Partition Scheme -> Press on Start -> Confirm that everything on the USB will be erased.<br/>
Software tools needed: Rufus

Option 2: Download and install the preferred Windows ISO file from Microsoft.  [The Link for Windows 11](https://www.microsoft.com/en-us/software-download/windows11) -> Start CMD as an Administrator -> <br/> Enter following commands: __Diskpart -> List Disk -> Select disk x (replace x with USB Drive number) -> Clean -> Create Partition Primary -> Select Partition 1 -> Active -> Format FS=NTFS quick -> Assign -> Exit__  -> Open the ISO File for it to be a directory -> Assuming the directory is F: (Could be different please check) __type f: in cmd -> type 'cd boot' -> Type 'bootsect /nt60 d: (d: is the USB Drive, could be different use your USB Drive Letter) -> Type 'exit' -> type 'xcopy f: \ *. * d: \ / E / H / F'__

__Can you do multiple boots from one key?__<br/>
Yes, you can use a bootloader. One Example for it is Ventoy. <br/>
<br/>
Ventoy is an open source tool to create bootable USB drive for ISO/WIM/IMG/VHD(x)/EFI files.
With ventoy, you don't need to format the disk over and over, you just need to copy the image files to the USB drive and boot it. You can copy many image files at a time and ventoy will give you a boot menu to select them.
