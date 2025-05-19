# 📸 Responsive Images with `srcset` in HTML

Using `srcset` in HTML is a best practice to deliver responsive and optimized images across different devices and screen resolutions.

## ✅ Why Use `srcset`

- Serve appropriately sized images for mobile, tablet, and desktop
- Improve performance and load time
- Support Retina (HiDPI) displays
- Improve SEO and Core Web Vitals

---

## 🔧 Syntax

```html
<img src="image-800.jpg"
     srcset="image-400.jpg 400w,
             image-800.jpg 800w,
             image-1200.jpg 1200w"
     sizes="(max-width: 600px) 400px,
            (max-width: 900px) 800px,
            1200px"
     alt="Responsive image example">
````

### Explanation:

* `srcset`: List of image sources with their width descriptors.
* `sizes`: Hints for browser to choose the best image depending on the viewport.
* `src`: Fallback image if browser does not support `srcset`.

---

## 🖥️ For Retina / High DPI Displays

```html
<img src="photo.jpg"
     srcset="photo.jpg 1x,
             photo@2x.jpg 2x"
     alt="High-resolution image example">
```

### Use this when you want to provide higher-resolution images for HiDPI screens like Retina MacBooks and modern smartphones.

---

## 📱 Responsive with `<picture>` Element

```html
<picture>
  <source media="(min-width: 800px)" srcset="large.jpg">
  <source media="(min-width: 400px)" srcset="medium.jpg">
  <img src="small.jpg" alt="Responsive with picture">
</picture>
```

### Useful when you want to change image **aspect ratio** or **format** (e.g., WebP vs JPG) depending on device.

---

## ⚠️ Best Practices

* Always provide `alt` text for accessibility.
* Optimize your images before uploading.
* Use a CDN or build process to generate multiple sizes automatically.
* Test across different screen sizes and devices.

---

## 💬 Resources

* [MDN Web Docs on srcset](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images)
* [Google Web.dev – Responsive Images](https://web.dev/serve-responsive-images/)

---
