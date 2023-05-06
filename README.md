# DolphinDB & Monk

This repository contains Monk.io template to deploy DolphinDB either locally or on cloud of your choice (AWS, GCP, Azure, Digital Ocean).

## Prerequisites

- [Install Monk](https://docs.monk.io/docs/get-monk)
- [Register and Login Monk](https://docs.monk.io/docs/acc-and-auth)
- [Add Cloud Provider](https://docs.monk.io/docs/cloud-provider)
- [Add Instance](https://docs.monk.io/docs/multi-cloud)

### Make sure monkd is running

```bash
foo@bar:~$ monk status
daemon: ready
auth: logged in
not connected to cluster
```

## Clone Repository

```bash
git clone https://github.com/monk-io/monk-dolphindb
```

## Load Template

```bash
cd monk-dolphindb
monk load MANIFEST
```

### Let's take a look at the themes I have installed

```bash
foo@bar:~$ monk list dolphindb
✔ Got the list
Type      Template             Repository  Version  Tags
runnable  dolphindb/dolphindb  local       -        -
```

## Deploy Stack

```bash
foo@bar:~$ monk run dolphindb/dolphindb
```

## Variables

The variables are in `dolphindb.yml` file. You can quickly setup by editing the values here.

| Variable  | Description      | Default |
| --------- | ---------------- | ------- |
| image_tag | Docker image tag | v2.00.9 |
| db_port   | Database port    | 8848    |

## Stop, remove and clean up workloads and templates

```bash
monk purge -a
```
