# End of Life - Repository Deprecated
**Important Notice:** This repository is no longer actively maintained or supported. No further issues or pull requests will be considered or approved. The content provided here is for historical reference only.

## Thank You
Thank you contributors and Greenbone community. Your dedication, feedback, and contributions have been invaluable.

\- SCS

---
---

![GVM Logstash Logo](https://github.com/SCS-Labs/Images/raw/main/GVM%20Logstash.png)

This docker image contains logstash configured to pull data from a Greenbone Vulnerability Manager instance.

Must login first using

```docker login docker.pkg.github.com```

Example command:

```sh
docker run -d \
-e DB_PASSWORD=<GVM postgres database password> \
-e DB_USER=gvm \
-e DB_HOST=<IP or Hostname for the GVM postgres database> \
-e ES_HOST=<IP or Hostname for elasticsearch> \
-e ES_USER=<Username for elasticsearch> \
-e ES_PASSWORD=<Password for elasticsearch user> \
--name gvm-logstash \
docker.pkg.github.com/secure-compliance-solutions-llc/gvm-logstash/gvm-logstash:master
```



| Environment Variable Name | Default Value           |
| ------------------------- | ----------------------- |
| `DB_HOST`                   | `gvm`                     |
| `DB_USER`                   | `gvm`                     |
| `DB_PASSWORD`               |                         |
| `ES_HOST`                   | `https://example.com:443` |
| `ES_USER`                   | `gvm-logstash `           |
| `ES_PASSWORD`               |                         |
