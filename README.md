# Complete EDIFY/update-binary Replacement
*[by osm0sis @ xda-developers](http://forum.xda-developers.com/member.php?u=4544860)*

makes flashable zips universal by using a shell script; thus not requiring a compiled update-binary.

> for an extensive how to, please have a look at [forum.xda-developers.com](http://forum.xda-developers.com/android/software-hacking/dev-complete-shell-script-flashable-zip-t2934449 "Jump to the forum entry").

##Included Functions:

```
ui_print "<message>" ["<message 2>" ...]

show_progress <amount> <time>
set_progress <amount>

sleep <seconds>

is_substring <substring> <string>

less_than_int <x> <y>
greater_than_int <x> <y>

mount <partition>
unmount <partition>
is_mounted <partition>

write_raw_image <file> <block>

package_extract_file <file> <destination_file>
package_extract_dir <dir> <destination_dir>

rename <file> <destination_file>

delete <file> [<file2> ...]
delete_recursive <dir> [<dir2> ...]

symlink <file/dir> <link> [<link2> ...]

set_metadata <file> <uid|gid|mode|capabilities|selabel> <value> [<uid|gid|mode|capabilities|selabel_2> <value2> ...]
set_metadata_recursive <dir> <uid|gid|dmode|fmode|capabilities|selabel> <value> [<uid|gid|dmode|fmode|capabilities|selabel_2> <value2> ...]

set_perm <owner> <group> <mode> <file> [<file2> ...]
set_perm_recursive <owner> <group> <dir_mode> <file_mode> <dir> [<dir2> ...]

ch_con <context> <file> [<file2> ...]
ch_con_recursive <dir_context> <file_context> <dir> [<dir2> ...]
restore_con <file/dir> [<file2/dir2> ...]

file_getprop <file> <property>
getprop <property>

sha1_check <file> [<sha1_hex> [<sha1_hex2> ...]]

apply_patch <src_file> <tgt_file> <tgt_sha1> <tgt_size> [<src_sha1_1>:<patch1> [<src_sha1_2>:<patch2> ...]]
apply_patch_check <file> [<sha1_hex> [<sha1_hex2> ...]]
apply_patch_space <bytes>

abort [<message>]
assert "<command>" ["<command2>"]

choose <time> <command1> <command2> [<default>]

backup_files <file> [<file2> ...]
restore_files <file> [<file2> ...]
```

# For Developers
Contributions are welcome! For feature requests and bug reports please [submit an issue](https://github.com/doppelhelix/android_update-binary_replacement/issues/new) or get in touch on [xda-developers](http://forum.xda-developers.com/android/software-hacking/dev-complete-shell-script-flashable-zip-t2934449 "Jump to the forum entry").

### Release flow

`develop -> master`

1. All work is done on branch `develop`.
2. If No errors occur the code is ready to be merged into `master`.

**Note: To avoid clutter, code that executes functions is not allowed in this repository.**
