- clear ipcs1 - using `ipcrm`
```
for x in `ipcs -m | grep $USER | awk '{ print $2 }'`; do ipcrm -m $x; done;
for x in `ipcs -s | grep $USER | awk '{ print $2 }'`; do ipcrm -s $x; done;
for x in `ipcs -q | grep $USER | awk '{ print $2 }'`; do ipcrm -q $x; done;
```
 `ipcrm -m` : removes shared memory
 `ipcrm -s` : removes semaphores
 `ipcrm -q` : removes message queues


