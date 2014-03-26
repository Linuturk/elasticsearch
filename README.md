Elasticsearch
========

Deploys elasticsearch 0.90.x on Debian or Red Hat based distros (tested on CentOS and Ubuntu).

Requirements
------------

Any pre-requisites that may not be covered by the ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

To Do
------------

- iptables work in this role does NOT play nice with other roles

Notes
------------
While using ```group_by key={{ansible_distribution}``` is a best practice in playbooks, we commonly see that abstracting a playbook out into a role on Galaxy makes use of the pattern ```when: ansible_os_family == "Debian"``` on including os-specific tasks. This allows playbooks to decide to run roles on specific OS families, but within roles, OS family-specific tasks are included using ```when:```. I feel that this makes sense as it is difficult to distribute roles that only 'half-work' because they have common and OS specific components that must both be called out in a task.

From #ansible:
```
(09:23:15 AM) sivel: smithmb: that is basically it.  sharable roles would make it harder, as it would put a lot of ownership on the person using the roles to use group_by and such correctly
(09:23:27 AM) sivel: smithmb: easier to use 'when' in the way you describe
(09:26:11 AM) sivel: smithmb: np, and I don't think you are doing it wrong for the sake of galaxy.  I think there are just 2 standards, defined by whether it is an easily shareable role or not
(09:26:52 AM) sivel: you could of course define that people had to use group_by, but I think that would be prohibitive for most users as it makes implementing it more difficult
```

License
-------

BSD

Author Information
------------------

Martin Smith <martin.smith@rackspace.com>
Mike Martin <mike.martin@rackspace.com>

[Rackspace - the open cloud company](http://rackspace.com)
Ask about our DevOps Automation Service - [www.rackspace.com/devops](http://rackspace.com/devops)
