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
  - A **snapshot file** is `YOUR DEFINITION HERE`.
  - A **backup level** is `YOUR DEFINITION HERE`.
  - A **level 0 backup** is `YOUR DEFINITION HERE`.

- **Exercise 2**

  ```bash
  # Insert the solution commands for Exercise 2 below
  ```

### Cron
#### Managing cron
Please paste the contents of `backup-cron-jobs.txt` in the space below.

  ```bash
  # Paste the contents of `backup-cron-jobs.txt` below
  ```
