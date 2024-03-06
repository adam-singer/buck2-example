### Instructions
- Create the executable files and send them to the remote (not cached):

`buck2 run -v 5 --ui re --ui debugevents --ui dice --ui io --remote-only --event-log /tmp/buck2_events.log //:test_bin|grep test.sh`
- Kill buck2 and clean the local cache:

`buck2 killall && buck2 clean`
- Run again (shows cached in CAS):

`buck2 run -v 5 --ui re --ui debugevents --ui dice --ui io --remote-only --event-log /tmp/buck2_events.log //:test_bin|grep test.sh`
- Check the output file from the above command

`ls -al` the file loaded from CAS from the previous command showing it has executable bit
