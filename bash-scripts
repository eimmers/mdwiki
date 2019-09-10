=== find all java versions on local filesystem
```
#!/bin/bash

FILES="`find / ! -fstype nfs ! -fstype cifs  -type f -executable -name java -exec sh -c "file -i '{}' | grep -q 'x-executable; charset=binary'" \; -print`"
for y in $FILES
do
echo "`$y -version 2>&1  | head -n 1`,`hostname`,$y"
done

RUNNING="`ps -fC java | awk '{print $8}' | grep -v ^CMD | sort | uniq`"
for y in $RUNNING
do
test -L $y
if [ "$?" == "0" ] ; then
LINK="LINK=`ls -l $y | awk '{print $NF}'`"
else
LINK=NOLINK
fi
echo "`$y -version 2>&1  | head -n 1`,`hostname`,$y,RUNNING,$LINK"
done
```
