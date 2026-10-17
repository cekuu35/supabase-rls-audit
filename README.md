# supabase-rls-audit

Free, read-only SQL audit for Supabase Row Level Security policies. Run it against
your own database (nothing leaves your machine) and it flags:

- tables where RLS is disabled
- tables with zero policies
- policies leaning on using (true)
- tables reachable by non / uthenticated that probably shouldn't be

## Usage

\\\ash
psql "\" -f audit/rls-audit.sql
\\\

Or paste udit/rls-audit.sql into the Supabase SQL editor. Read-only; no writes.

## What this doesn't cover

Write-side checks (with check), multi-tenant isolation, and storage.objects
policies. For those, the full **RLS Audit Kit** () packages 7 commented SQL
audits + a 60-check workflow + report templates:

https://cengokurtoglu.gumroad.com/l/supabase-rls-audit-kit

Want it done for you? From , ~2-day turnaround:
https://www.upwork.com/services/product/2083862107074689176

## License

MIT. Free forever.
