# Multiple Entries

You can split your slides.md into multiple files and organize them as you want using the `src` attribute.

#### `slides.md`

```markdown
# Page 1

Page 2 from main entry.

---
src: ./subpage.md
---
```

<br>

#### `subpage.md`

```markdown
# Page 2

Page 2 from another file.
```

[Learn more](https://sli.dev/guide/syntax.html#multiple-entries)

---

# Page Mermaid

```mermaid {scale: 0.75, alt: 'History of Web'}
timeline
    title History of Web
    section 1993-2004
        Web 1.0: ...
        Web 2.0 (1998-): Yahoo, Ebay, Gmail
    section 2004-2020
        Web 2.0: Yahoo, Ebay ...
        Web 3.0 (2009-): Facebook, Groupon, Airbnb 
    section 2020-Present 
        Web 3.0: ... 
```