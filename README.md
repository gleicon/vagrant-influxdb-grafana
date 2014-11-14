# InfluxDB + Grafana sandbox

Runs a VM with influxdb and grafana. You can use dashboard.yml and roles to install in a production server, just tune influxdb address.

# Requirements

    - Vagrant
    - Ansible installed locally
    - Internet connection

# Usage
## Locally with Vagrant

```
$ vagrant up 
$ open http://192.168.33.21 # on your browser
```

## Remotely with your cloud of preference
    
    - Add your hostname to ansible hosts file (/etc/ansible/hosts or any other location, you can change that)
        [dashboard]
        host1 ansible_ssh_host=192.168.1.1

    - Make sure you can ssh into it using keys
        ssh root@192.168.1.1

    - Run 
        ansible-playbook -l host dashboard.yml

    - Send me a pull request in case it doesn't works.

