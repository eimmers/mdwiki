
### default exit action with emailing the error
```
  trap_action()
  {
  echo "Script interrupted with Ctrl-C...please rerun, or manually cleanup leftove
  rs" >> $MAILLOG
  exit_action
  }

  exit_action()
  {
  echo "`date +%H:%M:%S`: Exiting" >> $MAILLOG
  echo "`date +%H:%M:%S`: Exiting"
  echo "" >> $MAILLOG
  echo "$ERROR" >> $MAILLOG
  echo "" >> $MAILLOG
  mailx -s "FAILED: $MAILTOPIC" $MAILEE < $MAILLOG
  exit 1
  }

trap trap_action HUP INT QUIT TERM

hammer csvvv content-hosts --export --file $OUTPUT || { ERROR="hammer command failed"  ; exit_action; }

```




