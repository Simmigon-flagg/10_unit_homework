# 10_unit_homework
# Submission

### Tar
#### Stripping Components
- **Exercise 2**
  - Extract `Movies`: `tar -xvf TarDocs.tar --strip-component=1 "TarDocs/Movies"`
  - Extract `Movies/ZOE_0004.mp4`: `tar -xvf TarDocs.tar --strip-component=2 "TarDocs/Movies/ZOE_0004.mp4"`

#### Modifying Archives
- **Exercise 1**

```bash
  # Insert the solution commands for Exercise 1 below
tar cvf update.tar 'sample.tar' 'mynames.tar'
tar -tf update.tar
touch test1.txt test2.txt
tar rvf update.tar test1.txt
tar rvf update.tar test2.txt
tar -tf update.tar
```

- **Exercise 2**

```bash
  # Insert the solution commands for Exercise 2 below
echo "latest">>  test2.txt
tar uvf update.tar test2.txt
tar -tf update.tar

```

- **Exercise 3**

```bash
  # Insert the solution commands for Exercise 3 below
tar -f update.tar --delete test1.txt
tar -tf update.tar
```

#### Incremental Backups
- **Exercise 1**
  - A **snapshot file** is `an incremental archive with additional metadata stored in a standalone file`.
  - A **backup level** is `after the first backup all others are incremental. It's a point in time snapshot`.
  - A **level 0 backup** is `the first backup preformed`.

- **Exercise 2**

```bash
  # Insert the solution commands for Exercise 2 below
tar --create --file=archive.1.tar --listed-incremental=/var/log/home.snar --level=0 /home/student

touch ~/new_file.1 ~/new_file.2

tar --list-incremental=/var/log/home.snar --level=1 /home/student
cp -a /var/log/home.snar /var/log/home.snar-1

tar tf /var/log/home/snar

Yes, I see my expected outcome

```

### Cron
    #Part 1
        */2 * * * * echo "Complete" >> snan.txt >/dev/null 2>&1
        * 17 * * * tar -cvzf document-backup.tar.gz ~/Documents >/dev/null 2>&1
        * 17 * * 5 tar -cvjf pictures-backup.tar.bz2 ~/Pictures >/dev/null 2>&1
    #Part 2
        (cd ~/data/cron/Documents && tar cvf ~/data/cron/cronjob.tar $(find . -type f -iname "*.txt"))
        mkdir -p ~/data/cron/exercises && tar xvf ~/data/cron/cronjob.tar -C ~/data/cron/exercises
    Part 4: Disable and Backup
        */2 * * * TUE,THU,SAT (cd ~/data/cron/Documents && tar cvf ~/data/cron/cronjob.tar $(find . -type f -iname "*.txt")) && mkdir -p ~/data/cron/exercises && tar xvf ~/data/cron/cronjob.tar -C ~/data/cron/exercises >/dev/null 2>&1
