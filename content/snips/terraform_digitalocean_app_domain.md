---
title: "terraform, digitalocean, apps, domain"
date: 2022-02-15T23:10:00+01:00
draft: false
---

```terraform
resource "digitalocean_domain" "this" {
  name = "asdomare.com"
}

resource "digitalocean_app" "development" {
  spec {

  # ...

    domain {
      name = "subdomain.asdomare.com"
    }

  # ...

  }
}

resource "digitalocean_record" "this" {
  type   = "CNAME"
  name   = "submain"
  domain = digitalocean_domain.this.id
  value  = "${replace(digitalocean_app.this.default_ingress, "https://", "")}."
}
```
