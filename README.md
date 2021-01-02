## Part-1 UTS namespace isolation understanding

$> git checkout part-1
$> make
// Only user namespace can be done without sudo
$> sudo ./isolate sh
// above commands gets into new shell
%> hostname
blah 1 (original)
%> hostname blah 2
%> hostname
blah 2
// On a different shell
$> hostname
blah 1

## Part-2 User Namespace

$> git checkout part-2
$> make
// Note, no need of sudo!
$> ./isolate sh
// above command gets into new shell
%> whoami
root
// get process id
%> echo $$
blah
// 
%> cat /proc/blah/uid_map
0 uid 1
%> exit
// Now, comment call to "prepare_userns" in isolate.c inside main method
// Repeat the above steps
// This suggests the importance of userns setup needed before creating isolation

## Part-3  Mount Namespace [Filesystem - minimal linux-alpine]
