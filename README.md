# Deluge Ansible role [![Ansible Lint](https://github.com/namelivia/ansible-deluge/actions/workflows/ansible-lint.yml/badge.svg)](https://github.com/namelivia/ansible-deluge/actions/workflows/ansible-lint.yml)

The project depends on the collection `community.docker` but apparently this [cannot be listed as a dependency](https://github.com/ansible/ansible/issues/62847) so make sure you add it to your `requirements.yml` file like:

```yml
---

collections:
  - community.docker

roles:
  - src: https://github.com/namelivia/ansible-deluge
```

## Required variables
 - `cloudwatch_region` Cloudwatch region to send the logs to.
 - `cloudwatch_log_group` Cloudwatch log group to send the logs to.
 - `deluge_downloads_folder` Path for the downloads.
 - `deluge_movies_folder` Path for the movies.
 - `deluge_tv_folder` Path for the series.
 - `backup_day` Day of the week in which the config will be backed up.
