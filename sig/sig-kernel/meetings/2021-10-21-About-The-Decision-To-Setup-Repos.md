# October 6, 2021 at 14:30pm GMT+8

## Agenda
- Talk about the way 
the kernel-sig to support storage-management-related features

## Attendees
- [@ninalijiaxin](https://gitee.com/ninalijiaxin)
- [@zhangzhiwi](https://gitee.com/zhangzhiwi)
- [@esay-to-see](https://gitee.com/esay-to-see)
- [@bubble_mao](https://gitee.com/bubble_mao)
- [@chenjinglong-hw](https://gitee.com/chenjinglong-hw)
- [@im-off-this-week](https://gitee.com/im-off-this-week)
- [@karl-z](https://gitee.com/karl-z)

## Notes
The kernel sig will take charge of ohos' storage management. It's duty include but not limited to:

1. Enable softwares to access files, whether local or distributed, intra-sandbox or inter-sandbox.
1. Eanble softwares to manage disks, whether statically mounted or dynamically mounted.
1. Provide necessary tools to operate filesystems and disks.

## Action items
- Setup the repo named `storage_user_file_manger` on `storage/user_file_manger`
- Setup the repo named `storage_app_file_manager` on `storage/app_file_manager`
- Setup the repo named `storage_app_fileshare_manager` on `storage/app_fileshare_manager`
- Setup the repo named `storage_storage_manager` on `storage/storage_manager`
- Setup the repo named `storage_distributed_file_manager` on `storage/distributed_file_manager`
- Setup the repo named `storage_fs_tools` on `storage/fs_tools`
- Setup the repo named `third_party_f2fs-tools` on `third_party/f2fs-tools`
- Setup the repo named `third_party_ntfs-3g` on `third_party/ntfs-3g`
- Setup the repo named `third_party_fsck_msdos` on `third_party/fsck_msdos`
- Setup the repo named `third_party_gptfdisk` on `third_party/gptfdisk`
- Setup the repo named `third_party_newfs_msdos` on `third_party/newfs_msdos`