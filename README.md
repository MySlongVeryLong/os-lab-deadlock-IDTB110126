
# Level 1

[[Pasted image 20260323133828.png]]

In this level, we were able to build an ext4 file system on those two files, and used user-space disk tool to create looped devices and mapped them to the file, and we were also able to mount them as a virtual drive  using udisksctl mount.

# Level 3

[[Pasted image 20260323140754.png]]

in this level, the sync_up successfully acquired the lock for mount_alpha and sync_down simutaneously acquried the lock for mount_alpha, after both finish its sleep, they both tried to acquire each other vault, which was already held by their own lock, therefore both processes stayed hung indifintely, since none of them will release the lock they already have hold of, plus, the OS is unable to force them to give up the lock. 

[[Pasted image 20260323143632.png]]
