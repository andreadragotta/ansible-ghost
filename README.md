# Ansible Ghost

## Host Vars

ghost.yml
```
---
ghost_setup_skip_ssl: False

ghost_letsencrypt_user: user@example.com

ghost_project_domain: localhost
ghost_project_url: "http://{{ ghost_project_domain }}"
ghost_project_url_secure: "https://{{ ghost_project_domain }}"
ghost_user_name: ghost
ghost_user_group: ghost
ghost_db: mysql
ghost_db_host: localhost
ghost_db_user: "{{ ghost_user_name }}"
ghost_db_name: "{{ ghost_user_name }}"
ghost_db_password: "{{ ghost_db_user }}"
ghost_smtp: SMTP
ghost_smtp_service: Mailgun
ghost_smtp_user: ''
ghost_smtp_password: ''
ghost_smtp_port: 2525
```

init.yml
```
---
user: demo
group: demo
user_password: password
```

database.yml
```
---
mysql_root_password: mypassword
```
