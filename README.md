# Ansible Role: rsnapshot

Setup local [rsnapshot](http://rsnapshot.org/). With a hourly/daily/weekly/monthly snapshots.

Tested on Ubuntu 16.04.

## Role Variables

The following variables can be used to customize the role:

    rsnapshot_root: 

Directory where the snapshots are to be stored.


    rsnapshot_hourly_interval: 4

Number of hours between each snapshot.

    rsnapshot_monthly_retain: 6

Number of monthly snapshot to retain.

    rsnapshot_directories: []

List of directories to to take snapshots of.

## Example Playbook

```yaml

- hosts: master
  become: yes

  roles:

    - role: roles/rsnapshot
      rsnapshot_root: /snapshots
      rsnapshot_directories:
        - /etc
        - /home
```

## License

MIT
