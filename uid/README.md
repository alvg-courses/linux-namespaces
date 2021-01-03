## Part-2 User Namespace
```
$> git checkout part-2
$> make
```
 Note, no need of sudo!
```
$> ./uid sh
```
 above command gets into new shell
```
%> whoami
root
```
 get process id
```
%> echo $$
blah
%> cat /proc/blah/uid_map
0 uid 1
%> exit
```
 Now, comment call to "prepare_userns" in isolate.c inside main method
 Repeat the above steps
 This suggests the importance of userns setup needed before creating isolation

