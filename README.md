# system
* 5 GB root partition
* 256Mb di RAM
* 1 CPU

# software
* alpine system
	* openssh
		* ``apk add openssh``
		* ``mkdir /root/.ssh && wget https://github.com/Xelk.keys > /root/.ssh/authorized_keys``
	* vim
		* ``apk add vim``
	* borg
		* ``apk add borgbackup``

# mounts
* root: 5GB
* /mnt/data : 200GB for data of borg backup
* /mnt/backup: usb disk 
* backup  with borg /mnt/data on /mnt/backup

# init borg
* ``rm -rf /mnt/data/ && borg init --encrypt=repokey /mnt/data/``
