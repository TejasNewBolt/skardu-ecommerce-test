# 🛍️ Skardu E-commerce Test Website

## 📋 **Purpose**

This is a **multi-page e-commerce website** specifically designed to test Skardu's multi-page snapshot generation system. Unlike many test websites that use hash navigation (#about, #contact), this site features **real working links** between **separate HTML pages**.

## 🎯 **Why This Website is Perfect for Testing**

### **✅ Real Multi-Page Architecture**
- **8+ separate HTML files** with unique content
- **Working navigation** between all pages (not hash anchors)
- **Internal linking** for proper page discovery
- **Mobile-first responsive** design

### **📄 Pages Included:**
1. **Homepage** (`index.html`) - Main landing page with navigation
2. **Shop Page** (`shop.html`) - Product listing page
3. **About Page** (`about.html`) - Company information
4. **Contact Page** (`contact.html`) - Contact form and information
5. **Privacy Policy** (`privacy-policy.html`) - Privacy terms
6. **Terms of Service** (`terms-of-service.html`) - Terms and conditions
7. **Product Detail Pages**:
   - `product-headphones.html` - Premium Wireless Headphones
   - `product-watch.html` - Smart Fitness Watch
   - `product-phone.html` - Phone Case Pro

## 🔗 **Live Website**

**URL**: `https://tejasnewbolt.github.io/skardu-ecommerce-test/`

## 🧪 **Testing Features**

### **✅ What Makes This Perfect for Skardu Testing:**
- **Real page navigation** (not single-page with hash routing)
- **Multiple link discovery methods**:
  - Main navigation menu
  - Footer links
  - Breadcrumb navigation
  - Internal content links
  - Product detail links
- **SEO-optimized structure**:
  - Proper meta tags
  - Semantic HTML
  - Mobile-first design
  - Fast loading times

### **🎯 Expected Snapshot Generation:**
Skardu should discover and create snapshots for **all 8+ pages** when testing with this website:

```
✅ index.html (Homepage)
✅ shop.html (Shop page)
✅ about.html (About page) 
✅ contact.html (Contact page)
✅ privacy-policy.html (Privacy page)
✅ terms-of-service.html (Terms page)
✅ product-headphones.html (Product detail)
✅ product-watch.html (Product detail)
✅ product-phone.html (Product detail)
```

## 🔧 **Technical Details**

### **Framework Detection:**
- **Type**: Static HTML (Generic)
- **Responsive**: Mobile-first design
- **SEO**: Optimized meta tags and structure

### **Navigation Structure:**
```
Homepage
├── Shop → Product Details
├── About
├── Contact
├── Privacy Policy
└── Terms of Service
```

### **Link Discovery Methods:**
1. **Header Navigation** - Main menu links
2. **Footer Links** - Secondary navigation
3. **Internal Content** - CTA buttons and text links
4. **Breadcrumbs** - Page hierarchy navigation

## 🎉 **Success Criteria**

When Skardu processes this website, it should:
1. ✅ **Discover all 8+ pages** through multiple link sources
2. ✅ **Create individual snapshots** for each page
3. ✅ **Detect "Generic HTML" framework** correctly
4. ✅ **Generate mobile-optimized** snapshots
5. ✅ **Complete processing** without errors

## 🚀 **How to Test**

1. **Add to Skardu Database**:
   ```sql
   INSERT INTO sites (domain, status) 
   VALUES ('tejasnewbolt.github.io/skardu-ecommerce-test', 'active');
   ```

2. **Run Multi-Page Generation**:
   - Skardu worker will discover pages via sitemap + crawling
   - Should find 8+ pages with working navigation
   - Each page will get its own snapshot in R2 storage

3. **Verify Results**:
   - Check R2 bucket for multiple snapshot files
   - Confirm each page has unique content and proper optimization

---

**🔥 This website solves the "broken navigation" problem that was preventing proper multi-page testing!** 🔥

Built for: **Skardu Technical SEO SaaS**  
Purpose: **Multi-page snapshot generation testing**  
Architecture: **Real pages, real navigation, real testing** ✅