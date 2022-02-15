---
title: "terraform, digitalocean, apps, domain"
date: 2022-02-15T23:10:00+01:00
draft: false
---

```terraform
data "digitalocean_domain" "this" {
  name = "domain"
}

resource "digitalocean_record" "this" {
  domain = data.digitalocean_domain.this.id
  type   = "CNAME"
  name   = "iam"
  value  = "${replace(digitalocean_app.this.default_ingress, "https://", "")}."
}
```
