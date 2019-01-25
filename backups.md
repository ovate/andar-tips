---
layout: default
---

## Why are backups more important for RM than most other programs?

#### By [Andar](https://forums.rpgmakerweb.com/index.php?members/andar.11882/), 7 Sep 2015


"Failed to load data" - "unexpected file format" - a few of you have already got those messages when trying to open their project, and repairing that project then often results in partial data loss.
The only way to prevent this is to use backups. You might read my starting point tutorial for this as I've linked automatic backup scripts there.

But why does this happen? Especially why does it happen to RM more often than to other programs you own, and still is a Windows problem that no one can solve?

To understand that, you first have to know how windows and your harddrive work.


Saving (and reading) data from the magnetic disc inside your harddrive takes time - it is one of the slowest tasks that a computer performs, and that usually slows down a lot of other processes.
Because of this all harddrives use a special cache to speed up the access - that is RAM memory where changed data is temporarily stored for quick windows access while the slow harddisc falls behind.

One of the reasons for the shutdown sequence of windows is to give the HDD controller time to save that cache onto the magnetic harddisc before it is lost by power off.
If that time is not there (for example due to a windows crash or because you cut the power instead of waiting for shutdown), then the data from the cache is not saved to the file, and the file can't be opened again later. You can only replace it with a backup file.
But because it's Windows and the HDD Controller that handle the cache and the data saving from cache to magnetic disc, nothing inside the RM editor can influence this or prevent the data damage.


But I can almost hear your questions "why does this only happens with RM and not with my other programs?" or "why does this happen to RM so much more often than with other programs I work longer with?".

No, RM is not unique in this - but it belongs to a special group of programs that need a permanent file access. Most database programs (for example Filemaker as another program with the same effect) require this because they need to handle data in a different way.
Your other programs? They can load the entirety of their data into your RAM and then close the file while working with the data. Some programs use temporary files to handle this while closing the original file.

But with most database programs that is not possible, they need the database files permanently open to access all data. And as long as the file is open for access, the HDD controller can not write the cache parts to the magnetic disc and close the file.
That is what increases the risc of a damaged file whenever windows crashes while the editor is open, or even if it crashes a short while after the editor is closed.

But we cannot change that - the disadvantages of regular file access in case of programs that handle a lot of data would cause more problems and riscs.
So I suggest you learn to keep backups of your game projects.

[back](./)
