raspberrypi-sixfab
==================

Download source code::

  $ git clone https://github.com/pabelanger/raspberrypi-sixfab
  $ cd raspberrypi-sixfab

Create hosts file, this will contain the IP address to your raspberrypi::

  $ cp inventory/hosts.example inventory/hosts
  $ vi inventory/hosts

Bootstrap tox virtualenv::

  $ tox -evenv --notest
  $ source .tox/venv/bin/activate

Run ansible-playbook::

  (venv) $ ansible-playbook -v -i inventory/hosts playbooks/site.yaml --ask-pass
