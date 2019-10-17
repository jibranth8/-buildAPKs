Should you find APKs that build with buildAPKs in the NUNAMES and NWNAMES files and elsewhere, please pull in ONAMES, UNAMES and an appropriate ma.bash file.  This means that two pull requests can be submitted!  One in buildAPKs, by adding a name to the corresponding ONAMES or UNAMES file.  And the second pull in an appropriate module repository by adding an `_AT_` line in the ma.bash file. 

1) To see the available ma.bash files you can use: 
```
find ~/buildAPKs/sources/ -type f -name ma.bash -exec cat {} \;
```

2) The line of interest in ma.bash is: 
```
find ~/buildAPKs/sources/ -type f -name ma.bash -exec cat {} \; | grep _AT_
```

	Usage: `_AT_ org/repo commit`

	Usage: `_AT_ user/repo commit`


Adding information to ONAMES, UNAMES and the corresponding ma.bash file will enhance this progect and its' user experience.  The file ~/buildAPKs/.gitmodules has information about the repository associated with a particular ma.bash file.  For the curious, the `_AT_` function is located in `grep -r _AT_ ~/buildAPKs/scripts/` after the first APKs have been built, and the corresponding submodules have been cloned.


The following files are located in ~/buildAPKs/conf/:

| File Name | Purpose   |
| --------- | --------- |
| GAUTH     | OATH token file |
| NUNAMES   | Names with possible new APKs that might migrate to ONAMES, UNAMES and ma.bash. |
| NWNAMES   | Names with possible new APKs that might migrate to ONAMES, UNAMES and ma.bash. |
| ONAMES    | Organizations whose APKs build in buildAPKs on device. |
| README.md | This file |
| TNAMES    | Topics that have APK projects which build with buildAPKs on device. |
| UNAMES    | Users whose APKs build in buildAPKs on device. |
| VERSIONID | Current buildAPKs Version |
<!-- README.md EOF -->