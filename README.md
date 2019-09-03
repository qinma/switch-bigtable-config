Create files at ~/.google/bigtable/
```
.cbtrc.p13n
.cbtrc.dev
.cbtrc.prod
```

Put script file switchbigtable at ~/cmds/. This file will force to create a symlinks ~/.cbtrc to point to one of files you created above.

Make swithcbigtable executable by runing command 
```
chmod 755 swtichbigtable
```

Switching bigtable default config file
```
switchbigtable p13n
```

Example:
```
$ switchbigtable p13n
Previous: lrwxr-xr-x 1 qma staff 39 Sep 3 11:14 /Users/qma/.cbtrc -> /Users/qma/.google/bigtable/.cbtrc.prod
Current: lrwxr-xr-x 1 qma staff 39 Sep 3 11:14 /Users/qma/.cbtrc -> /Users/qma/.google/bigtable/.cbtrc.p13n

$ switchbigtable dev
Previous: lrwxr-xr-x 1 qma staff 39 Sep 3 11:12 /Users/qma/.cbtrc -> /Users/qma/.google/bigtable/.cbtrc.p13n
Current: lrwxr-xr-x 1 qma staff 38 Sep 3 11:13 /Users/qma/.cbtrc -> /Users/qma/.google/bigtable/.cbtrc.dev

$ switchbigtable prod
Previous: lrwxr-xr-x 1 qma staff 38 Sep 3 11:14 /Users/qma/.cbtrc -> /Users/qma/.google/bigtable/.cbtrc.dev
Current: lrwxr-xr-x 1 qma staff 39 Sep 3 11:14 /Users/qma/.cbtrc -> /Users/qma/.google/bigtable/.cbtrc.prod
```


