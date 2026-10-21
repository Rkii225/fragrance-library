# Strata

Single self-contained file: index.html. No build step, no dependencies.

House rules
- British English in all text (colour, organise, modelled, neighbour).
- No em dashes anywhere in page copy or documents.
- Keep the DATA line byte-identical unless Richard asks for a data change.
- Never invent notes, sources, reviewer quotes or prices. If unsure, say so and ask.
- Name the structural approach and why before any significant change.
- Ask before: pushing, changing visibility, deleting data, adding dependencies.

Checks before every commit
- Syntax check: awk '/<script>/{f=1;next}/<\/script>/{f=0}f' index.html > /tmp/s.js && node --check /tmp/s.js
- Em dash check: grep -c $'\u2014' index.html must print 0
- Counts load as 44 bottles, 84 formulas, 11 trios, 34 with occasion notes

Notes
- The repo is public and served by GitHub Pages.
- User data lives in browser localStorage. Export and import is the only sync.
- The Downloads copy and this repo can drift. Ask which is the source of truth.
