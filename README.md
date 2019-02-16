# rhelsysupdate
---

## Descritpion
Playbook to continously update RHEL host(s) until no more updates are found.
Each run logs the changes to the output directory with ctime stamps. 
Root access is required to target host(s) and is enforced by *ansible.cfg*.

## Invocation
It is recommented to have shared keys to run this playbook.

```ansible-playbook main.yml -e "inventory_group=<inventory group/host name>"```

If the user password has to be passed in, the '-k' option can be passed in.

```ansible-playbook rhelsysupdate.yml -k -e "inventory_group=<inventory group/host name>"```

## File Structure
Under the 'output' directory exist '*.keep*' hidden file for directory
scaffolding. The 'output' directory is used to house log files from runs that
do not need to exist in version control.

```
rhelsysupdate/
├── README.md
├── ansible.cfg
├── handlers
│   └── rhelsysupdate.yaml -> ../tasks/rhelsysupdate.yaml
├── main.yaml
├── output
│   └── .keep
└── tasks
    ├── checkforupdate.yaml
    └── rhelsysupdate.yaml

3 directories, 7 files
```
