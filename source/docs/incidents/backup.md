# Implementing a backup plan

Backups are one of those things that some people don’t seem to take seriously until it’s too late. Data
loss can be a catastrophic event for an organisation, so it’s imperative that you implement a solid
backup plan. 

There’s no one best backup solution, since it all depends on what kind of data you need to secure, and
what software and hardware resources are available to you. This may mean that you’ll need to make some compromises, such as creating regular snapshots of
your database server’s storage volume or regularly dumping a backup of your important databases to
an external storage device.

The `rsync` utility is one of the most valuable pieces of software around to server administrators. It
allows us to do some really wonderful things. In some cases, it can save us quite a bit of money. For
example, online backup solutions are wonderful in the sense that we can use them to store off-site
copies of our important files. And depending on the volume of data, they can be quite expensive.
With `rsync`, we can back up our data in much the same way, with not only our current files copied over
to a backup target but also differentials. If we have another server to send the backup to, even better.