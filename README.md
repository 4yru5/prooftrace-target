# InvoiceFlow (ProofTrace demo target)

A tiny invoice service, used as the demo target for
[ProofTrace](https://github.com/4yru5/prooftrace). Structured as a
HackBench-style challenge: a Dockerized app with a planted flag.

```bash
docker compose up --build   # http://localhost:8000
```

The branch `add-invoice-endpoint` opens a PR that adds
`GET /api/invoices/{invoice_id}` — authenticated, parameterized SQL, and
vulnerable to Broken Object Level Authorization (CWE-639). ProofTrace reviews
that PR and proves the exploit live.
