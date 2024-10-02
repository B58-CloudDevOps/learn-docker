1) Add the disk ( On UI )  or create the instance with 40gg 
2) Expand the disk : sudo growpart /dev/nvme0n1 4 ( 4 is the partition number ) ; expands the partition
3) sudo lvexpend -l +50%FREE /dev/mapper/RootVG-varVol ( Extends LVM )
4) sudo sudo lvextend -l +100%FREE /dev/mapper/RootVG-homeVol  ( Extends LVM )
5) sudo xfs_growfs /var ; sudo xfs_growfs /home                        ( Expand the fileSystem ) 
6) df -h
