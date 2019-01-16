# msc

`msc` are my "missing shell commands"; things that I use regularly, have in
my muscle memory, and dearly miss when I don't have.

I regularly use `msc` when setting up a new server to make my life easier:

*  Download `msc` as e.g., `/tmp/msc`
*  When root: `perl /tmp/msc install`
*  When not: `mkdir ~/bin; perl /tmp/install ~/bin`
*  Next, edit `~/.bashrc` and add:

   ``` shell
   /usr/local/bin/msc install > /tmp/$$ && . /tmp/$$ && rm /tmp/$$
   # or ~/bin/msc install, if that's the location where msc resides
   ```

What this does (below list may be stale):

```
  color     output text in terms with colors, try 'color' to see usage
  l, d      short, long directory listing
  lt, dt    short, long listing by date
  lx, dx    short, long directory listing by extension, e.g. dx c (lists *.c)
  rx	    remove files by extension, e.g. rx o a (removes *.o *.a)
  up1, up2  cd 1 or 2 up, use as: eval `up1` and: eval `up2`
            to set up the aliases - and --, run the bootstrap or:
      	      eval `up_aliases`
  gd        goto-directory, use as: eval `gd /new/directo/ry`
      	    to set this up as a bash function, run the boostrap or:
      	      gd_function > /tmp/$$; . /tmp/$$; rm -f /tmp/$$
  xd        fast cd, use as: eval `xd ulb` (ulb is short for
            /usr/local/bin or whatever matches)
            to set this up as a plain xd bash command, run the boostrap or:
              xd_function > /tmp/$$; . /tmp/$$; rm -f /tmp/$$

  tarc	    create tar archive, supported: .tar, .tar.gz, .tgz, .tar.bz2, .tbz2
  tart	    list tar archive
  tarx 	    extract tar archive

  path      set shell path, use as: eval `path d1 d2 d3`, sets standard dirs
            and adds to the path d1,d1/bin,d1/sbin and so on
  ps1       set bash prompt, use as: eval `ps1`

  x         start xterm, use as: x user@host, default: thisuser, @localhost
  xoff      turn off X ($DISPLAY), use as: eval `xoff`
  xon       turn on X  ($DISPLAY), use as: eval `xon`
  	    to set up xon and xoff as aliases, run the boostrap or:
	      eval `xoff_xon_aliases`
  hisgrep   show shell history (use his STRING to limit)
            to set this up, run the boostrap or:
              hisgrep_function > /tmp/$$; . /tmp/$$; rm -f /tmp/$$

  e, ew     start editor (async or wait mode)
  ep        edit and reload bash profile, use as: eval `ep`
  	    to set up ep as a bash command, run the boostrap or:
	      eval `ep_alias`
  cpf       copy-forward, if you don't have cp -n
  ftail     like tail -f, if you don't have it
  ip        shows IP addresses
  ruler     displays a 80-column ruler, or use ruler -w WIDTH for other nrs.
  man       man display in a new window
  m         make, with stdout/stderr to less
  perldoc   Perl documentation in a new window
  psg       like 'ps ax' but looks for certain commands
  while1    run commands every 1 second (or 5 sec with while5, or without delay
              with while0), use as: while1 cmd1 cmd2 cmd3
  beep      sound the alarm
  ascii     shows the ASCII table
  localtime converts seconds-since-epoch to local time
  gmtime    converts seconds-since-epoch to UTC (gm) time
  timet     shows seconds-since-epoch
  ds        case-insensitive find, avoids .svn, CVS etc.
  loglimit  pipe that writes limited logs, use as:
              cmd | loglimit FILE SIZE HISTORYFILES

  b64enc    encode into base64 format (either cmdline arguments or stdin)
  b64dec    decode from base64 format (either cmdline arguments or stdin)
  hex       hexdumps a file (use - for stdin)
  crypt     standard Unix crypt function

  d2u,u2d   dos2unix or unix2dos file conversions
  tolower   file renaming to lower case
  tac       reversed cat, dumps file line by line in reversed order
  rsyncdir  rsync over ssh to sync local and remote dir
  stripws   delete trailing whitespace in file(s) or stdin

  r         sudo to root, optional arguments are a command to root
  h         with arguments, search for in /etc/hosts; else, edit the file
  k         starts python(3) to do kalkulations or similar
```
