backend:
  name: github
  repo: your-github-username/inarilife-store
  branch: main

media_folder: "assets/images"
public_folder: "assets/images"

collections:
  - name: "products"
    label: "Products Catalogue"
    folder: "content/products"
    create: true
    slug: "{{slug}}"
    fields:
      - {label: "SKU Code", name: "sku", widget: "string"}
      - {label: "Product Title", name: "title", widget: "string"}
      - {label: "Original Title / Source", name: "original_title", widget: "string", required: false}
      - {label: "Category", name: "category", widget: "select", options: ["Kitchen & Dining", "Everyday Gadgets", "Home Organisation & Storage", "Travel & Outdoors", "Cleaning & Household Essentials", "Toys", "Car Accessories"]}
      - {label: "Subcategory", name: "subcategory", widget: "string", required: false}
      - {label: "MRP (₹)", name: "mrp", widget: "number", value_type: "float"}
      - {label: "Selling Price (₹)", name: "selling_price", widget: "number", value_type: "float"}
      - {label: "Amazon Product URL", name: "amazon_url", widget: "string", required: false}
      - {label: "Main Image", name: "main_image", widget: "image"}
      - {label: "Gallery Images", name: "gallery_images", widget: "list", required: false}
      - {label: "Product Video URL", name: "video_url", widget: "string", required: false}
      - {label: "Short Description", name: "short_description", widget: "text"}
      - {label: "Full Description", name: "full_description", widget: "markdown"}
      - {label: "Key Features", name: "features", widget: "markdown"}
      - {label: "Specifications", name: "specifications", widget: "markdown"}
      - {label: "Featured on Homepage", name: "featured", widget: "boolean", default: false}
      - {label: "Product Status", name: "status", widget: "select", options: ["Active", "Coming Soon", "Draft", "Archived"], default: "Coming Soon"}
      - {label: "SEO Title", name: "seo_title", widget: "string", required: false}
      - {label: "SEO Meta Description", name: "seo_description", widget: "text", required: false}
      - {label: "URL Slug", name: "slug", widget: "string"}