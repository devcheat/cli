Diskpart Commandl ine 

```cmd
Diskpart
 
create vdisk file="e:\MyDocs.vhd" maximum=1024 
select vdisk file="e:\MyDocs.vhd"
attach vdisk
create partition primary
format fs=ntfs label="MyDocs" quick
active
assign
```
