# RAID-Day

## Part 1 - Creating Drives  
Create two (or more) EBS volumes in the EC2 instance.  
Attach the volumes  
```:~$ sudo apt install mdadm```  
  

## Part 2 - Creating the Array  
```sudo mdadm --create /dev/md0 --level=0 --raid-devices=2 /dev/xvdf /dev/xvdg```  
  
Create Mount Point  
  
```sudo mkdir /data```  
```sudo mount /dev/md0 /data```
