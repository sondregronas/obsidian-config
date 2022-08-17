<%*
  let title = tp.file.title
  if (title.startsWith("Untitled")) {
    title = await tp.system.prompt("Title");
    await tp.file.rename(`${title}`);
  } 
  tR += "---"
%>
title: <%* tR += `${title}` %>
aliases: 
  - <%* tR += `${title}` %>
lang: nb-NO
authors:
  - Sondre Grønås
created: <%tp.file.creation_date("YYYY-MM-DD HH:mm:ss")%>
updated: <%tp.date.now("YYYY-MM-DD HH:mm:ss")%>
---
# <%* tR += `${title}` %>
Denne uken jobbet vi med:
<% tp.file.cursor() %>

## Gjøremål

## Ukens innlegg
- Ingen merkverdige artikler eller videoer denne uken.

### Utforskningslenker
- Ingen merkverdige ting å utforske denne uken
