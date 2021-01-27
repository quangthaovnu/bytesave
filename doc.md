## Document BYTESAVE ##

1. Licence
 Function: Active licence
 bytesave active.licence "licence"
 return:
 if success:
    show(expiration date)
 else:
    show(error)

 2. Connect
 Function: add connect
 bytesave add.connect "connect name" "connect string"
 return:
  if success:
    show(connect name, username, data used, connect string)
  else:
    show(error)

Function: edit connect
bytesave: edit.connect "connect name"
return:
if success:
    show connect affter update(connect name, username, data used, connect string)
else:
    show(error)

Function: delete connect
bytesave delete.connect "connect name"
return:
if success:
    show(msg delete connect "connect name" success)
else:
    show(error)

Function: show connect
bytesave show.connect "connect name"
return:
    if success:
        show(connect name, username, data used, connect string)
    else:
        show(error)

Function: show all connect
bytesave list.connect
return:
    if success:
        show all list name connect
    else:
        show(error)

3. backup

Function: add task backup
bytesave add.backup "name task" "path local" "name connect" "list day of week{}" "time"
// if day of week NOT NULL then schedule backup at time on day of week.
// if day of week NULL them schdule backup after time of day.

Function: edit task backup
bytesave edit.backup "name task"
return:
    if success:
        show msg success
    else:
        show msg error

Function: delete task backup
bytesave delete.backup "name task"
return:
    if success:
        show msg success
    else:
        show msg error

Function: show task backup
bytesave show.backup "name task"
return:
    if success:
        show( name task, path local, name connect, list day of week, time)
    else:
        show msg error

Function: show list backup
bytesave list.backup
return:
    if success:
        show list name task backup
    else:
        show msg error

4. restore




