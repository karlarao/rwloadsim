## Quick start of the oltp sample workload

 * Install the RWP\*Load Simulator and set environment variables properly.
 * Make sure you have gnuplot and a http server installed and running.
 * If at all possible, create a repository that is not in your database under test.
 * Create a database for your testing.
 * Decide upon a short project name (could be the same as your database) and copy
the two files oltp.env and oltp.rwl using your project name to your working directory.
 * Edit these two files according to the comments in them.
Note that the latter file with rwl suffix often is referred to as your projects paramter file.
 * Create the awr directory and results directory.
 * Prepare your http server such that the awr directory is visible from a browser.
 * Run ```oltpverify -ds``` to verify directories and dba access to your database.
 * Run ```oltpcreate``` to create schemas.
 * Run ```oltpverify -a``` for a complete verification of database scheamas.
 * Run ```oltpcore``` as your first run
 * Verify you can browse results from this run

You will now be ready to do real runs that may include:

 * Running ```oltprun``` for individual runs
 * Modifing paramters in your projects parameter file
 * Doing scaling runs using ```oltpscale```
 * Running continuous runs using ```oltpforever```

Note that most scripts take a -H option to provide a brief help.

All reference guides is available as rwlman pages, start with ```rwlman oltp```
