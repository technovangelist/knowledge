# How would i like to process notes and do something useful with them? I don't have this figured out yet.
<script src='https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js'></script><div class=mermaid>
graph TD
A((Things I want to remember)) --> AV   & Paper[Paper Media] & Online[Online Reading]  & Social[Social Media] 
Social --> Discord & Slack & Twitter
Online --> Kindle & Articles[Online Articles] & PDF
AV --> Video[Video Content] & Podcasts
Video --> YiNote[Take notes in YiNote]
YiNote --> YiNoteExport[Press Button to Export to Markdown]
YiNoteExport --> Obsidian((Obsidian))
Podcasts --> Airr[Take notes in Airrcast]
Airr --> ProcessAirr[Process the AirrQuotes]
ProcessAirr --> Readwise
PDF --> Todo
Kindle --> KindleNotes[Take notes in the Kindle app]
KindleNotes --> Readwise
Articles --> Instapaper & Hypothesis & Memex
Instapaper --> Readwise
Hypothesis -->Readwise
Twitter --> Todo
Discord --> Todo
Slack --> Todo
Paper -->|Take Photo in Readwise| Readwise
Memex --> Obsidian
</div>
