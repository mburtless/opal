# OPAL Security

This document will specify OPAL security configuration and the reasoning behind it.

**TBD this week.** For now mentioned briefly in the getting started with docker tutorial.

OPAL is ready for production security-wise.

<!-- Security considerations:
* OPAL server should **always** be protected with a TLS/SSL certificate (i.e: HTTPS).
  * Meaning: the traffic between OPAL client and OPAL server should always be encrypted (it's ok to terminate SSL in the load balancer).
  * Why:
    * The client can verify the identity of the server using the HTTPS certificate.
    * To protect yourself from MITM / Sniffing attacks. OPAL server **may** pass autentication tokens and other secrets to OPAL client, if the client need such secrets in order to fetch data.
* OPAL server should **always** run in secure mode - meaning JWT token verification should be active.
  * Why:
    * So that the server may verify the identity of the client. The client may gain access to sensitive secrets pushed from the server, so we want to prevent anyone unauthorized from pretending to be a client.
    * So that the server may verify the identity of a `datasource` (someone pushing data updates). That way we prevent an attacker from infecting your OPA state with malicious data.
* OPAL server should be configured with a **master token**.
* Sensitive configuration variables (i.e: environment variables with sensitive values) should **always** be stored in a dedicated **Secret Store**
  * Example secret stores: AWS Secrets Manager, HashiCorp Vault, etc.
  * If you use infrastructure-as-code to spin your environments such as terraform, **NEVER EVER EVER** store secrets as part of your source code (e.g: in your git repository). -->