# ExpenseOwl (LazyCat LPK)

Minimal expense tracker with budgets, categories and charts.

- Upstream: https://github.com/Tanq16/ExpenseOwl
- Image: `tanq16/expenseowl:v4.1` (mirror mode, digest-matched)
- License: MIT (full text in `content/licenses/LICENSE`)
- Containers: single (JSON backend under /app/data)

## Notes

- Upstream has **no account system**: configuration lives in the web UI at `/settings`,
  and access control is expected to come from a reverse proxy. In LazyCat that is the
  entry-point auth, which is why `usage` explicitly warns not to disable it or share the URL.
- Default backend is JSON (`STORAGE_TYPE` unset); Postgres is optional and not used here.
- All data is plain JSON under `/app/data`, persisted on `/lzcapp/var/data`.
- Port 8080 in-container.
- Not yet verified on a real device.
