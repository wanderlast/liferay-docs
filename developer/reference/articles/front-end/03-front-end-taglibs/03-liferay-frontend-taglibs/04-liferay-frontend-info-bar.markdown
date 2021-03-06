---
header-id: liferay-front-end-info-bar
---

# Liferay Front-end Info Bar

[TOC levels=1-4]

An info bar provides a button that toggles the visibility of additional sidebar 
information. This is perfect for providing more detailed metadata for a search 
result, such as the file size, type, URL, etc. 

![Figure 1: The info bar tags create a sidebar panel toggler that reveals additional info.](../../../../images/liferay-frontend-taglib-info-bar-article.png)

The configuration has two key parts: the info bar---and buttons---and the
sidebar panel. 

Info bar:

```html
<liferay-frontend:info-bar>
  <liferay-frontend:info-bar-buttons>
    <liferay-frontend:info-bar-sidenav-toggler-button
      icon="info-circle"
      label="my info"
    />
  </liferay-frontend:info-bar-buttons>
</liferay-frontend:info-bar>
```

The `<liferay-frontend:info-bar-sidenav-toggler-button>` tag uses 
[Clay Icons](/docs/7-2/reference/-/knowledge_base/r/clay-icons) 
for the `icon` attribute. 

Sidebar panel:

```html
<div class="closed container-fluid-1280 sidenav-container sidenav-right" id="<portlet:namespace />infoPanelId">
    <liferay-frontend:sidebar-panel>
      <div>
      <h2>sidebar content</h2>
      <p>Here is some content</p>
      </div>
    </liferay-frontend:sidebar-panel>
</div>
```

Note that the sidebar panel's wrapper `<div>` has the classes `closed` and 
`sidenav-right`. The info button toggles the classes `open` and `closed`, 
showing and hiding the sidebar panel. The `sidenav-right` class specifies that 
the panel should open on the right.

![Figure 2: The info bar tags create a sidebar panel toggler that reveals additional info.](../../../../images/liferay-frontend-taglib-info-bar.png)

The examples above use some of the available attributes. See the 
[info bar](@app-ref@/foundation/latest/taglibdocs/liferay-frontend/info-bar.html), 
[info bar buttons](@app-ref@/foundation/latest/taglibdocs/liferay-frontend/info-bar-buttons.html), 
[info bar sidenav toggler button](@app-ref@/foundation/latest/taglibdocs/liferay-frontend/info-bar-sidenav-toggler-button.html), 
and 
[sidebar panel](@app-ref@/foundation/latest/taglibdocs/liferay-frontend/sidebar-panel.html) 
taglibdocs for the full list of available attributes for the tags. 

## Related Topics

- [Liferay Front-end Add Menu](/docs/7-2/reference/-/knowledge_base/r/liferay-front-end-add-menu)
- [Liferay Front-end Cards](/docs/7-2/reference/-/knowledge_base/r/liferay-front-end-cards)
- [Liferay Front-end Management Bar](/docs/7-2/reference/-/knowledge_base/r/liferay-front-end-management-bar)

