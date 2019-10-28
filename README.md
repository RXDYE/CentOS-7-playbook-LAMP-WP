# CentOS-7-playbook-LAMP-WP
This is a LAMP + Wordpress playbook for Ansible. It configures LAP+W and MySql on separate servers.

Playbook vars should be placed at group_vars/all.yml:
---
db_name: wordpress

mysql_wp:
  user: wpuser
  password: wppassword
  priveleges: "{{db_name}}.*:ALL"
  user_host: '%'
  host: database-host
