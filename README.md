# ansible-xsos
Ansible playbook to run xsos on a set of servers

Get Started
1. Clone this repository
2. Add your list of servers to the hosts file in the server group
3. Make any additional changes to ansible.cfg that might be relevant to your environment (e.g. changing the remote_user)
4. Run the playbook (ansible-playbook playbook.yml)

The playbook assumes that you have ansible installed and that you are cloning the repo to the control node.  It also assumes your control node has access to the internet to pull down the xsos binary.  It pulls this file down to the control node, distributes it to the servers in the servers group, runs xsos on each server, fetches the results, and then cleans up the files that it created.  The only thing that should be remaining is the reports in /tmp/fetched.
