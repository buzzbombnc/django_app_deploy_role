django_app_deploy_role
======================

Role that deploys a Django application from Git repository onto a server.

Requirements
------------

* Python virtualenv installed.

Role Variables
--------------

The following variables are defined in vars/main.yml:

| Variable         | Default | Description                                                                    |
|:----------------:|:-------:|:-------------------------------------------------------------------------------|
|apache_autostart  | true    |Autostart on server restart?                                                    |
|apache_restart    | true    |(Re)start on install?                                                           |
|apache_ssl_enabled| true    |Base SSL enabled?  Only enables modules.  Certificates are on a per-site basis. |

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: apache_role }

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
