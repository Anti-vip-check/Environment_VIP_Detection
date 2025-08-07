## configure tips


### requirements
pixel4 

kernel version：4.14.170-g5513138224ab-ab6570431

System Oparation: Android 10(QQ3A.200805.001)

kernel moule:environment-detection.kpm.kpm



## test case

### steps1 
push the module to android device ad enable the module in Apatch framework(https://github.com/bmax121/APatch)


### steps2
Install the target apk and run 

### steps3
Enter adb mode and view kernel logs

command: dmesg -C |grep pattern(supply:"root path","checking proc files:","EmulatorDetect","/system/build.prop")


[ 3346.588349] Process accessing root path: /system/xbin/su, pid: 14746, tgid: 891, comm: <unknown>, user_lr: 0x765be464a8, user_fp: 0x7ff23a36c0
[ 3347.913793] Process checking root path: /data/local/xbin/su, pid: 14772, tgid: 891, comm: <unknown>, user_lr: 0x75fd5c9d8c, user_fp: 0x75fbcd9d10
[ 3347.913838] Process checking root path: /system/bin/su, pid: 14772, tgid: 891, comm: <unknown>, user_lr: 0x75fd5c9d8c, user_fp: 0x75fbcd9d10
[ 3347.913892] Process checking root path: /system/sbin/su, pid: 14772, tgid: 891, comm: <unknown>, user_lr: 0x75fd5c9d8c, user_fp: 0x75fbcd9d10
[ 3347.913912] Process checking root path: /system/bin/failsafe/su, pid: 14772, tgid: 891, comm: <unknown>, user_lr: 0x75fd5c9d8c, user_fp: 0x75fbcd9d10
[ 3347.913927] Process checking root path: /system/sd/xbin/su, pid: 14772, tgid: 891, comm: <unknown>, user_lr: 0x75fd5c9d8c, user_fp: 0x75fbcd9d10
[ 3347.913942] Process checking root path: /system/xbin/su, pid: 14772, tgid: 891, comm: <unknown>, user_lr: 0x75fd5c9d8c, user_fp: 0x75fbcd9d10

[  711.190418] Process checking root path: /system/build.prop, pid: 6096, tgid: 891, comm: <unknown>, user_lr: 0x76e6712e54, user_fp: 0x75f0c97990
[  711.191175] Process checking root path: /system/build.prop, pid: 6096, tgid: 891, comm: <unknown>, user_lr: 0x76e6712e54, user_fp: 0x75f0c97990
[  711.195616] Process checking root path: /system/build.prop, pid: 6096, tgid: 891, comm: <unknown>, user_lr: 0x76e6712e54, user_fp: 0x75f0c97990
[  711.196100] Process checking root path: /system/build.prop, pid: 6096, tgid: 891, comm: <unknown>, user_lr: 0x76e6712e54, user_fp: 0x75f0c97990
[  711.200513] Process checking root path: /system/build.prop, pid: 6096, tgid: 891, comm: <unknown>, user_lr: 0x76e6712e54, user_fp: 0x75f0c979c0
[  711.200893] Process checking root path: /system/build.prop, pid: 6096, tgid: 891, comm: <unknown>, user_lr: 0x76e6712e54, user_fp: 0x75f0c979c0
[  711.203639] Process checking root path: /system/build.prop, pid: 6096, tgid: 891, comm: <unknown>, user_lr: 0x76e6712e54, user_fp: 0x75f0c95140
[  715.760700] Process checking root path: /system/build.prop, pid: 6005, tgid: 891, comm: <unknown>, user_lr: 0x76e6712e54, user_fp: 0x75fc97fb70
[  715.762348] Process checking root path: /system/build.prop, pid: 6005, tgid: 891, comm: <unknown>, user_lr: 0x76e6712e54, user_fp: 0x75fc9808f0
[  715.763621] Process checking root path: /system/build.prop, pid: 6005, tgid: 891, comm: <unknown>, user_lr: 0x76e6712e54, user_fp: 0x75fc9808f0


[ 1675.719439] Process checking proc files: /proc/self/maps, pid: 13555, tgid: 891, user_lr: 75fb698428, user_fp: 75fb263cc0
[ 1675.719463] Process accessing proc files: /proc/self/maps, pid: 13555, tgid: 891, user_lr: 75fb698428, user_fp: 75fb263cc0
[ 1676.303763] Process checking proc files: /proc/self/maps, pid: 13289, tgid: 891, user_lr: 76e6712e54, user_fp: 75ec249ba0
[ 1676.303785] Process accessing proc files: /proc/self/maps, pid: 13289, tgid: 891, user_lr: 76e6712e54, user_fp: 75ec249ba0
[ 1676.463956] Process checking proc files: /proc/self/maps, pid: 13439, tgid: 891, user_lr: 75fb68d428, user_fp: 75fb258cc0
[ 1676.463978] Process accessing proc files: /proc/self/maps, pid: 13439, tgid: 891, user_lr: 75fb68d428, user_fp: 75fb258cc0
[ 1676.919254] Process checking proc files: /proc/self/maps, pid: 13270, tgid: 891, user_lr: 75fb686428, user_fp: 75fb251cc0
[ 1676.919340] Process accessing proc files: /proc/self/maps, pid: 13270, tgid: 891, user_lr: 75fb686428, user_fp: 75fb251cc0
[ 1677.862428] Process checking proc files: /proc/self/maps, pid: 13554, tgid: 891, user_lr: 75fb6a832c, user_fp: 75fb360a30
[ 1677.862469] Process accessing proc files: /proc/self/maps, pid: 13554, tgid: 891, user_lr: 75fb6a832c, user_fp: 75fb360a30
[ 1678.821684] Process checking proc files: /proc/self/maps, pid: 13555, tgid: 891, user_lr: 75fb698428, user_fp: 75fb263cc0
[ 1678.821713] Process accessing proc files: /proc/self/maps, pid: 13555, tgid: 891, user_lr: 75fb698428, user_fp: 75fb263cc0
[ 1679.396812] Process checking proc files: /proc/2237/smaps_rollup, pid: 1464, tgid: 891, user_lr: 76e6712e54, user_fp: 75f4d23fd0
[ 1679.396834] Process accessing proc files: /proc/2237/smaps_rollup, pid: 1464, tgid: 891, user_lr: 76e6712e54, user_fp: 75f4d23fd0
[ 1679.575035] Process checking proc files: /proc/self/maps, pid: 13439, tgid: 891, user_lr: 75fb68d428, user_fp: 75fb258cc0
[ 1679.575059] Process accessing proc files: /proc/self/maps, pid: 13439, tgid: 891, user_lr: 75fb68d428, user_fp: 75fb258cc0
[ 1680.096906] Process checking proc files: /proc/self/maps, pid: 13270, tgid: 891, user_lr: 75fb686428, user_fp: 75fb251cc0
[ 1680.096933] Process accessing proc files: /proc/self/maps, pid: 13270, tgid: 891, user_lr: 75fb686428, user_fp: 75fb251cc0
[ 1680.369646] Process checking proc files: /proc/self/maps, pid: 13289, tgid: 891, user_lr: 76e6712e54, user_fp: 75ec249ba0
[ 1680.369669] Process accessing proc files: /proc/self/maps, pid: 13289, tgid: 891, user_lr: 76e6712e54, user_fp: 75ec249ba0
[ 1680.748251] Process checking proc files: /proc/self/maps, pid: 13438, tgid: 891, user_lr: 75fb69d32c, user_fp: 75fb355a30
[ 1680.748283] Process accessing proc files: /proc/self/maps, pid: 13438, tgid: 891, user_lr: 75fb69d32c, user_fp: 75fb355a30
[ 1681.943582] Process checking proc files: /proc/self/maps, pid: 13555, tgid: 891, user_lr: 75fb698428, user_fp: 75fb263cc0
[ 1681.943635] Process accessing proc files: /proc/self/maps, pid: 13555, tgid: 891, user_lr: 75fb698428, user_fp: 75fb263cc0
[ 1682.672715] Process checking proc files: /proc/self/maps, pid: 13439, tgid: 891, user_lr: 75fb68d428, user_fp: 75fb258cc0
[ 1682.672757] Process accessing proc files: /proc/self/maps, pid: 13439, tgid: 891, user_lr: 75fb68d428, user_fp: 75fb258cc0
[ 1683.252244] Process checking proc files: /proc/self/maps, pid: 13270, tgid: 891, user_lr: 75fb686428, user_fp: 75fb251cc0




[ 1940.363077] [EmulatorDetect] process <unknown> (pid: 14278, tgid: 891) is accessing /proc/cpuinfo, user_lr: 0x76e6712e54, user_fp: 0x75e1cbe2b0
[ 1943.467949] [EmulatorDetect] process <unknown> (pid: 14306, tgid: 891) is accessing /system/build.prop, user_lr: 0x75d6fc60e4, user_fp: 0x75d6aff010
[ 1944.034861] [EmulatorDetect] process <unknown> (pid: 14306, tgid: 891) is accessing /system/lib/libc_malloc_debug_qemu.so, user_lr: 0x75d6f0a574, user_fp: 0x75d6afd1d0
[ 1944.599159] [EmulatorDetect] process <unknown> (pid: 14306, tgid: 891) is accessing /system/lib/libc_malloc_debug_qemu.so, user_lr: 0x75d6f0a544, user_fp: 0x75d6afd1d0
[ 1944.599211] [EmulatorDetect] process <unknown> (pid: 14306, tgid: 891) is accessing /system/lib/libc_malloc_debug_qemu.so, user_lr: 0x75d6f0a574, user_fp: 0x75d6afd1d0
[ 1944.599440] [EmulatorDetect] process <unknown> (pid: 14306, tgid: 891) is accessing /system/lib/libc_malloc_debug_qemu.so, user_lr: 0x75d6f0a544, user_fp: 0x75d6afd1d0
[ 1944.599472] [EmulatorDetect] process <unknown> (pid: 14306, tgid: 891) is accessing /system/lib/libc_malloc_debug_qemu.so, user_lr: 0x75d6f0a574, user_fp: 0x75d6afd1d0
[ 1944.600048] [EmulatorDetect] process <unknown> (pid: 14306, tgid: 891) is accessing /system/lib/libc_malloc_debug_qemu.so-arm, user_lr: 0x75d6f0a544, user_fp: 0x75d6afd1d0
[ 1944.600092] [EmulatorDetect] process <unknown> (pid: 14306, tgid: 891) is accessing /system/lib/libc_malloc_debug_qemu.so-arm, user_lr: 0x75d6f0a574, user_fp: 0x75d6afd1d0
[ 1944.600742] [EmulatorDetect] process <unknown> (pid: 14306, tgid: 891) is accessing /system/lib/libc_malloc_debug_qemu.so, user_lr: 0x75d6f0a544, user_fp: 0x75d6afd1d0
[ 1944.600775] [EmulatorDetect] process <unknown> (pid: 14306, tgid: 891) is accessing /system/lib/libc_malloc_debug_qemu.so, user_lr: 0x75d6f0a574, user_fp: 0x75d6afd1d0
[ 1944.600805] [EmulatorDetect] process <unknown> (pid: 14306, tgid: 891) is accessing /dev/socket/qemud, user_lr: 0x75d6f0a544, user_fp: 0x75d6afd1d0
[ 1944.600835] [EmulatorDetect] process <unknown> (pid: 14306, tgid: 891) is accessing /dev/socket/qemud, user_lr: 0x75d6f0a574, user_fp: 0x75d6afd1d0


## steps4
Locate the specific detection address based on the user_lr address of the log and the maps file of the target process