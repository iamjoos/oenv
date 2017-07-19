# oenv
Shell script to set Oracle environment variables
You can also put the following to ~/.bash_profile to automatically create aliases for all your databases (change /home/oracle/oenv to actual location of the script):
```
for oraenv in $(grep -oP "^# ocfg \K\w+" /home/oracle/oenv |  sort | uniq | tr '[:upper:]' '[:lower:]')
do
    alias ${oraenv}=". /home/oracle/oenv ${oraenv}"
done
```
