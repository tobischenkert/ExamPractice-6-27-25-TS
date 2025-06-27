# Option 2

Download and install the preferred Windows ISO file from Microsoft.  [The Link for Windows 11](https://www.microsoft.com/en-us/software-download/windows11) -> Start CMD as an Administrator -> <br/> Enter following commands: __Diskpart -> List Disk -> Select disk x (replace x with USB Drive number) -> Clean -> Create Partition Primary -> Select Partition 1 -> Active -> Format FS=NTFS quick -> Assign -> Exit__  -> <br> 
Open the ISO File for it to be a directory -> Assuming the directory is F: (Could be different please check)
__type f: in cmd -> type 'cd boot' -> Type 'bootsect /nt60 d: (d: is the USB Drive, could be different use your USB Drive Letter) -> Type 'exit' -> type 'xcopy f: \ *. * d: \ / E / H / F'__
