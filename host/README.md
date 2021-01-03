## Part-1 UTS namespace isolation
```
$> git checkout part-1
$> make
```
 Only user namespace can be done without sudo
```
$> sudo ./host sh
```
 above commands gets into new shell
```
%> hostname
blah 1 (original)
%> hostname blah 2
%> hostname
blah 2
```
 On a different shell
```
$> hostname
blah 1
```

