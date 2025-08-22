# 🛍 Shopify E-commerce Project

## ✨ Features

### 🗂️ Navigation Flow
**Navbar:**
- Home
- Shop → shows all collections.

**Collections page:** displays all available collections.  
**Collection detail page:** shows products of that specific collection.  
**Product detail page:** preserves the collection path.

**Breadcrumb examples:**
- On a collection page → Home → Collection Name
- On a product page → Home → Collection Name → Product Name

### 🏠 Homepage
- **Sub-Collections Slider:** Large images, titles, and navigation arrows; clicking a card navigates to the collection page.
- **Bestsellers Section:** Dynamically showcases selected products.
- **General FAQs** displayed globally.

### 📦 Collections
- **Custom breadcrumb navigation:**  
  Home → Category → Product
- **Related Blog Posts Section:**  
  - Each collection can be linked to multiple blog posts.  
  - Blog posts displayed with thumbnail, title, and excerpt.  
  - Content dynamically populated via metaobjects/metafields.

### 🗂️ Collection Detail Page
**Breadcrumb:** Home → Collection Name  

**Content:**
- **Collection Title & Description**
- **Product List:** Products belonging to that collection
- **Related Articles (Blog Section):**
  - Shows blog posts related to the current collection  
  - Each post includes an image, title, and excerpt  
  - Content is pulled dynamically from collection metafields
- **FAQ Section:**
  - Priority: Collection-specific FAQs (from metafield `faq_groups`)  
  - If no collection FAQs exist → fallback to General Store FAQ

### 📝 Metaobjects & Metafields Reference

| Key                        | Type                                     | Applies To | Purpose                                                                 |
| -------------------------- | ---------------------------------------- | ---------- | ----------------------------------------------------------------------- |
| `custom.show`              | Boolean (True/False)                     | Collection | Toggles whether the collection should be visible in navigation.         |
| `custom.category_slider`   | Metaobject (Slider Item)                 | Collection | Defines sub-collection slider items (image, title, subtitle, link).     |
| `custom.breadcrumb_path`   | Collection reference (List)              | Collection | Defines breadcrumb hierarchy (e.g. Home → Shop → Collection → Product). |
| `custom.faq_groups`        | Metaobject (FAQ group)                   | Collection | Attaches FAQ groups per collection.                                     |
| `faq_group.items`          | Metaobject reference (List of FAQ items) | FAQ Group  | Connects multiple FAQ entries.                                          |
| `faq_item`                 | Metaobject                               | –          | Fields: **question (text)**, **answer (richtext)**.                     |
| `custom.related_blogposts` | Metaobject (related_blogpost)           | Collection | Shows related blog posts for the collection.                            |
| `related_blogpost`         | Metaobject                               | –          | Fields: **title**, **excerpt**, **image**, **article reference**.       |

### ⚙️ Technical Notes
- **Theme:** Dawn (latest)  
- **Custom Sections under `/sections`:**
  - `sub-collection-nav.liquid`
  - `faq-section.liquid`
  - `breadcrumb.liquid`
  - `related-blogposts.liquid`
- Fully responsive, tested on desktop & mobile  
- All content dynamically populated from **metafields/metaobjects** (no hardcoded values)

  # 🚀 Setup Notes

> **🌐 Live Store:** [GlowMart - Nazlı Özer Test Store](https://nazliozer-test.myshopify.com/)

### 1. Clone & Connect Project

```bash
git clone https://github.com/nazliozer/shopify-store
cd shopify-test
shopify theme dev
```

### 2. Configure Shopify Admin

Navigate to **Shopify Admin → Settings → Custom Data** and define the required metafields & metaobjects:


## 📄 Deliverables

- **Development store URL:** [https://nazliozer-test.myshopify.com/](https://nazliozer-test.myshopify.com/)
-   PASSWORD: glowmart  
- **Repository link:** [https://github.com/nazliozer/shopify-store](https://github.com/nazliozer/shopify-store)

