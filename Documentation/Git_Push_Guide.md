## Git Push Guide
### Abstract

This guide serves as a reminder to push measurements and any changes made to configurations or code to this repository. 

This is much the most convenient way to have the measurement data available at any time.

### Pushing to GitHub

Suppose you have made some enlightening measurements using the lab computer and want to push them to the repository.

Note: this will work just the same when ssh'd into the lab computer.  (refer to the Remote Access Guide for more information)

1. Open a terminal and navigate to the SPIKES directory:

```bash
cd ~/SPIKES
```

2. Pull the latest changes from the repository:

It is always possible some changes have been made to the repository since the last time you pulled. To avoid conflicts it is best to pull the latest changes before pushing.

```bash
git pull
```

3. Add the changes to the staging area:

This command will add all changes to the staging area. If you only want to add specific files you can replace the `.` with the file name.

```bash
git add .
```

4. Commit the changes:

This command will commit the changes to the local repository. The `-m` flag is used to add a (required) message to the commit.

```bash
git commit -m "Message describing the changes made"
```

5. Push the changes to the repository:

This command will push the changes to the repository. On the Lab computer you will not be required to enter your username and password every time you push.

```bash
git push
```
