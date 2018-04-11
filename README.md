# Rasberry Pi monitoring server

Create a Raspberry Pi monitoring server with Graphite + Grafana.

<img src="https://i.imgur.com/e5z3KWV.png" width="700px">

## Prerequisites

 * Ansible
 * Raspberry Pi (Only tested with Pi 3 Model B) 
 
You may want to change whisper's retention periods for your metrics in `roles/graphite/files/config/storage-schemas.conf`.
A few are provided with a default of:
```
pattern = .*
retentions = 1m:30d,10m:1y
```
 
## Running

Run the ansible playbook:

    ansible-playbook -K -u pi -i inventories/hosts site.yml
    
## Getting data

Here are some projects that let you create some graphite compatible data:

* [OhmGraphite](https://github.com/nickbabcock/OhmGraphite) (Windows PC stats)
* [collectd](https://collectd.org/) (Unix daemon)
