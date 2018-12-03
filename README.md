# rhelsysupdate
---

## Descritpion
Simple playbook to apply security updates and log the output to an "output"
direcotry for record keeping.

Root access is required to target host(s).

## Invocation
It is recommented to have shared keys to run this playbook.

```ansible-playbook rhelsysupdate.yml```

If the user password has to be passed in, the '-k' option can be passed in.

```ansible-playbook rhelsysupdate.yml -k```

## File Structure
Under the 'output' directory exist '.keep' hidden file for directory 
scaffolding. The 'output' directory is used to house log files from runs that
do not need to exist in version control.

```
.
├── ansible.cfg
├── output
├── README.md
└── rhelsysupdate.yml

1 directory, 3 files
```
