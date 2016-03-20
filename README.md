#### udubun1604adv
#####1
goto setup interface,press E to config.Add
```
linux /install/vmlinuz file=/cdrom/pressed/ubuntu-server.seed quiet --- priority=low 
```
//ask every question

choose location, press tab to continue

#####2
```
ssh install@10.0.2.10
```

choose export mode.->setup user and password->allow shadow password->  
allow login as root(no)

#####3
partition disks ->manual->SCSI2(0,0,0)sda->yes->GPT->  
Create EFI: choose freespace->create partition, type, like 500mb,->beginning-> use as EFI system partition (do these for each disk)
continue partition: For example,sda ,choose 50gb, beginning->pyisical volume for raid->done  
continue partition: choose 99%,....same as above


#####5
configure software RAID ->yes->create MD device->RAID1


