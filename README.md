# GRAVITY💠MEDIA

A futuristic social-media super-app foundation with a responsive Phase 1 interface.

## Current implementation

- Responsive desktop, tablet, and mobile application shell
- Space-inspired visual system: deep-space surfaces, electric cyan/blue/violet accents, orbit logo
- Desktop sidebar, discovery rail, and mobile bottom navigation
- Home feed with **For You**, **Following**, and **Latest** views
- Post composer with local persistence, text validation, character limit, and honest local-only status
- Like and bookmark interactions persisted in browser storage
- Profile surface and profile navigation
- Light/dark appearance toggle and reduced-motion support
- External **Gravity AI** button opens `https://gravity-ai-ask-anything.lovable.app/` in a new tab
- Empty states for planned surfaces instead of fake content or fake success states

## Run locally

This first vertical slice has no build step or dependency installation. Serve the repository with any static server, for example:

```bash
python3 -m http.server 8080
```

Then open `http://localhost:8080`.

## Honest status

This repository currently contains the frontend foundation and a browser-local demo state. It is **not yet production-ready**: authentication, a database, media storage, server-side authorization, real-time messaging, moderation, search indexing, and secure uploads require a configured backend and external services. The UI intentionally labels planned surfaces rather than pretending those systems are connected.

## Next engineering slice

1. Add Supabase (or an equivalent supported backend) for email/password auth, profiles, posts, comments, likes, follows, and row-level authorization.
2. Replace local composer state with verified server mutations and optimistic rollback.
3. Add secure media storage with MIME/size validation and signed access URLs.
4. Add integration and end-to-end tests for auth, authorization, feed privacy, and mobile navigation.

Do not add credentials to this repository. Configure them through deployment environment variables.
