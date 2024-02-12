
- app chart usage -- setting up ingress/traefik
```yaml
    certificate:
      commonName: "aimachina.io"
      dnsNames:
        - "aimachina.io"
        - "www.aimachina.io"
    ingressRoute:
      domain: aimachina.io
      matchingRule: Host(`aimachina.io`) || Host(`www.aimachina.io`)
      middlewares:
        - name: headers-middleware

      tls:
        secretName: tls-cert
```