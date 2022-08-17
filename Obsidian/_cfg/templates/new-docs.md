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
tags:
  - Definisjon
created: <%tp.file.creation_date("YYYY-MM-DD HH:mm:ss")%>
updated: <%tp.date.now("YYYY-MM-DD HH:mm:ss")%>
---
# <%* tR += `${title}` %>
<% tp.file.cursor() %>