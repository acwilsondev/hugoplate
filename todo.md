# Business Content Migration TODO

## Content Inventory
- [ ] Identify all existing business content that needs to be migrated
  - [ ] Homepage content (banner, features, services, etc.)
  - [ ] About page content (company info, team members, mission/vision)
  - [ ] Service/product pages
  - [ ] Blog posts/articles
  - [ ] Case studies
  - [ ] Testimonials
  - [ ] Contact information
  - [ ] Legal pages (privacy policy, terms of service)
- [ ] Organize content by priority (what needs to be migrated first)
- [ ] Identify and collect all media assets (images, videos, PDFs, etc.)
- [ ] Create a content spreadsheet that maps existing content to new Hugo structure

## Hugo Content Structure Requirements
- [ ] Understand Hugo content organization:
  - [ ] Content is organized in `content/english/` directory
  - [ ] Each section has its own folder (blog, about, etc.)
  - [ ] Section landing pages use `_index.md`
  - [ ] Individual pages use regular `.md` files
- [ ] Review required frontmatter for each content type:
  - [ ] Common: title, meta_title, description, draft status
  - [ ] Blog: date, image, categories, author, tags
  - [ ] Custom sections: may require specific frontmatter
- [ ] Map business content types to Hugo template sections

### Specific Frontmatter Requirements

#### Homepage (_index.md)
```yaml
---
# Banner
banner:
  title: "Main headline for the business"
  content: "Brief description or tagline"
  image: "/images/banner.png"
  button:
    enable: true
    label: "Call to Action Text"
    link: "/services" # or any appropriate link

# Features
features:
  - title: "Feature or Service #1"
    image: "/images/feature-1.png"
    content: "Description of the feature or service"
    bulletpoints:
      - "Key benefit 1"
      - "Key benefit 2"
      - "Key benefit 3"
    button:
      enable: true
      label: "Learn More"
      link: "/feature-1-details"
  
  # More features as needed
---
```

#### Blog Posts
```yaml
---
title: "Blog Post Title"
meta_title: "SEO-optimized title (if different)"
description: "Brief description for SEO"
date: 2025-04-11T10:00:00Z
image: "/images/blog-featured-image.png"
categories: ["Category1", "Category2"]
author: "Author Name"
tags: ["tag1", "tag2", "tag3"]
draft: false
---
```

#### About Page
```yaml
---
title: "About Us"
meta_title: "About [Company Name] | Our Story"
description: "Learn about our company history, mission, and values"
image: "/images/about-header.jpg"
draft: false
---
```

#### Services/Products Page
```yaml
---
title: "Our Services"
meta_title: "Professional Services | [Company Name]"
description: "Explore our range of professional services"
image: "/images/services-header.jpg"
draft: false
---
```

#### Contact Page
```yaml
---
title: "Contact Us"
meta_title: "Contact [Company Name] | Get In Touch"
description: "Reach out to our team for inquiries or support"
draft: false
---
```

## Layout and Design Requirements
- [ ] Review existing template layouts in `layouts/` directory
- [ ] Identify which layouts need customization for business content
- [ ] Create list of custom layout components needed
- [ ] Plan for custom shortcodes if needed (for specialized content blocks)
- [ ] Identify styling needs and Tailwind CSS customizations in `data/theme.json`
- [ ] Plan for responsive design considerations

## Content Migration Steps
1. [ ] Set up basic site configuration
   - [ ] Update `hugo.toml` with business information
   - [ ] Configure `config/_default/params.toml` with site parameters
   - [ ] Set up menus in `config/_default/menus.toml`
   - [ ] Customize theme colors and fonts in `data/theme.json`

2. [ ] Prepare the content structure
   - [ ] Create necessary content folders
   - [ ] Set up taxonomy (categories, tags) as needed

3. [ ] Migrate Home Page
   - [ ] Update `content/english/_index.md` with business banner and features
   - [ ] Add business-specific sections

4. [ ] Migrate Core Pages
   - [ ] About page
   - [ ] Services/Products pages
   - [ ] Contact page
   - [ ] Legal pages

5. [ ] Migrate Blog Content
   - [ ] Convert existing blog posts to Hugo markdown format
   - [ ] Add proper frontmatter (title, date, categories, etc.)
   - [ ] Optimize images and other media

6. [ ] Create Custom Components
   - [ ] Implement any custom shortcodes needed
   - [ ] Create custom layouts as required

7. [ ] Review and Test
   - [ ] Check content for formatting issues
   - [ ] Test on multiple devices for responsive design
   - [ ] Validate links and media
   - [ ] Check SEO elements (meta titles, descriptions)

## Technical Tasks
- [ ] Install required Hugo modules or dependencies
- [ ] Set up image processing pipeline
- [ ] Configure multilingual support if needed
- [ ] Set up SEO optimization
- [ ] Configure social media integration
- [ ] Set up form handling for contact forms
- [ ] Review and optimize site performance
- [ ] Set up build and deployment process

## Post-migration Tasks
- [ ] Create content update guidelines
- [ ] Document the content structure
- [ ] Train team members on updating the Hugo website
- [ ] Set up a content calendar for future updates
- [ ] Plan for ongoing maintenance

