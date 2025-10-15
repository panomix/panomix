# ADK Installation and Integration Guide

 **ADK** is a layer that runs **independently within the article body** on your news website.  

This means the script **should not be placed on the homepage, article listing pages, or other sections**—it must be inserted **only inside the article body**.


---

### ADK Installation Script

Add the following script inside your article body template, such as within `<article>` or `<div class="article-body">`.


```html
<script
  src="https://aisdk-js-fgaaagggamgjdsgm.z02.azurefd.net/scripts/adk/embed.min.js"
  data-wsid="Insert Workspace ID Here"
  async
></script>
```

| Attribute | Description |
| --- | --- |
| `src` | Fixed path to ADK |
| `data-wsid` | Your unique Workspace ID — provided individually to each publisher via email |
| `async` | Loads the script asynchronously so it won’t block page rendering |

---
### 📍 Example: Where to Insert Script

```html
<article class="article-body">
  <p>Your article content goes here.</p>
  <p>...</p>

  <!-- Insert ADK script here -->
  <script
    src="https://aisdk-js-fgaaagggamgjdsgm.z02.azurefd.net/scripts/adk/embed.min.js"
    data-wsid="Insert Workspace ID Here"
    async
  ></script>
</article>
```

---

### ⚠️ Important Notes

- Do not add this script to your homepage or article listing pages. ADK only works inside the article body.  

- Please keep your `data-wsid` (Workspace ID) private. Sharing this ID with anyone outside your organization can lead to security issues. If exposed, access to ADK may be temporarily suspended, so make sure only authorized personnel have access.

- Since the script loads asynchronously (async), no additional optimization is required.

---
## **Need Help?** ##

If you have any questions or run into issues with implementing the script, please contact info@panomix.io. We’ll get back to you quickly and help resolve any problems.



