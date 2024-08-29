VBoxManage createvm --name "KayosVM" --register
VBoxManage modifyvm "KayosVM" --memory 512 --ostype Other
VBoxManage storagectl "KayosVM" --name "IDE Controller" --add ide --controller PIIX4
VBoxManage storageattach "KayosVM" --storagectl "IDE Controller" --port 0 --device 0 --type dvddrive --medium path/to/iso
VBoxManage startvm "KayosVM" --type gui
