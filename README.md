django_app_deploy_role
======================

Role that deploys a Django application from Git repository onto a server.

Tasks:
1. Deploy repository to server.
2. Create virtualenv and requirements via `requirements.txt` file.
3. Create an `environment` file with any variables passed in via the `env_vars`.
4. Validate the Django application by using the `manage.py` script with the `check`, `test`, and `migrate` arguments.

Requirements
------------

* Python `virtualenv` and `pip` installed.
* The repository must contain a Django project!

Role Variables
--------------

The following variables are defined in vars/main.yml:

| Variable   | Required | Description                                |
|:-----------|:--------:|:-------------------------------------------|
| repository | true     | Git repository to deploy from.             |
| reference  | false    | Git reference to use.  Defaults to 'HEAD'. |
| directory  | true     | Deployment directory to use.               |
| env_vars   | false    | A dictionary of key-value env variables.   |

Note that if your `repository` utilizes SSH, you must have a key available for connection.

If you're using an SSH agent for connecting to your remote host and the git+SSH repository, you may need to add additional configuration to the Ansible inventory file:

    ansible_ssh_extra_args="-o ForwardAgent=yes"

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      vars:
        env_vars:
          whatever: "you need"
      roles:
         - { role: django_app_deploy_role, respository: "http://github.com/buzzbombnc/djangoapp", directory: "/deploy/dir" }

License
-------

MIT License

Copyright (c) 2017 Ken Treadway

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
