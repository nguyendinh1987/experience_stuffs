# work for me on ubuntu16
Step1: Create swap image, you can locate this file anywhere in your harddisks. For example, I create the file at /home/my_username/.extraswap
>> \# 1M means 1GB. You can set to any number, depending on how much space you have on your harddisk  
>> dd if=/dev/zero of=/home/my_username/.extraswap/swapfile.img bs=1024 count=1M

Step2: Bake the swap file
>> mkswap /media/fasthdd/swapfile.img

Step3: Bring up on boot (permanently and it is optional)
>> \# Add this line to /etc/fstab  
>> /media/fasthdd/swapfile.img swap swap sw 0 0

Step4: Activate  
>> sudo swapon /home/my_username/.extraswap/swapfile.img

Step5: Deactivate  
>> sudo swapoff /home/my_username/.extraswap/swapfile.img

# references  
- [askubuntu](https://askubuntu.com/questions/178712/how-to-increase-swap-space)
