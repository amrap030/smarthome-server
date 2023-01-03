## Usage

Install the dependencies:

```
ansible-galaxy install -r requirements.yml
```

Finally, run the playbook:

```
ansible-playbook run.yml -l your-host-here -K
```

The "-K" parameter is only necessary for the first run, since the playbook configures passwordless sudo for the main login user

For consecutive runs, if you only want to update the Docker containers, you can run the playbook like this:

```
ansible-playbook run.yml --tags="port,containers"
```
