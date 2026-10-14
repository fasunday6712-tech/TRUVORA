# TRUVORA Supabase setup

This folder contains the first secure connection package for the TRUVORA consumer/provider website.

## Included
- `index.html` — website configured with the supplied Supabase project URL and publishable key; registration and password sign-in use Supabase Auth.
- `schema.sql` — initial database schema, role/profile creation trigger, tables, indexes, and Row Level Security policies.
- `SETUP.md` — setup and testing instructions.

## Security notes
- The browser includes only the Supabase project URL and publishable key. This key is designed for public clients; it is not a secret.
- Never add a database password, `service_role` key, or secret API key to this folder or a public repository.
- The profile role is created from an allow-listed registration choice and is protected from self-editing. Roles are only `consumer` and `provider`; there is no admin role.
- Business verification status is guarded against client-side self-verification. A trusted server-side/admin verification workflow still needs to be built.
- RLS must remain enabled. Review policies and test with separate consumer and provider accounts before production launch.

## Current scope
Registration and login are connected. The consumer/provider pages are still portal landing pages; listing management, enquiries, saved providers, reviews, account recovery, provider verification, email delivery settings and full dashboards need their UI and workflows implemented before launch. Do not advertise the entire ecosystem as production-ready yet.
