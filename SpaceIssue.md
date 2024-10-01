1) Add the disk ( On UI ) 
2) Expand the disk : sudo growpart /dev/xvda 4 ( 4 is the partition number ) ; expands the partition
3) sudo lvextend -l +50%FREE /dev/mapper/RootVG-homeVol ; ( Extends LVM )
4) sudo lvextend -l +1000%FREE /dev/mapper/RootVG-varVol ; ( Extends LVM )
5) sudo xfs_growfs  /var ; sudo xfs_growfs  /hom                         ( Expand the fileSystem ) 
6) df -h
