# Landing Page Maintenance Guide

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<!-- Find this div in the header -->
<div class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    DH Enterprises  <!-- Replace this text -->
</div>
```

2. **Navigation Menu Items:**
```html
<div class="hidden lg:flex space-x-8">
    <!-- Update these link texts as needed -->
    <a href="#caracteristicas" class="text-gray-300 hover:text-white transition-colors">Características</a>
    <a href="#beneficios" class="text-gray-300 hover:text-white transition-colors">Beneficios</a>
</div>
```

### Hero Section
The main headline and subtitle can be updated here:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">
    <!-- Replace this headline -->
    Impulsando Empresas del Sur de Florida con Pagos Rápidos y Económicos
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    <!-- Replace this subtitle -->
    Pagos Instantáneos, Tarifas Bajas, Seguridad Nivel Bancario
</p>
```

### Understanding Tailwind Classes
Common classes used in this landing page:

- Text Sizes: `text-xl`, `text-2xl`, `text-3xl`, etc.
- Colors: `text-gray-300`, `bg-gray-900`
- Spacing: `px-6` (padding), `mb-8` (margin)
- Responsive Design: `md:text-5xl` (applies at medium screens)

To modify a style:
1. Find the element you want to change
2. Locate its class attribute
3. Modify existing classes or add new ones

Example:
```html
<!-- Original -->
<p class="text-xl text-gray-300 mb-12">

<!-- Modified for larger text and different color -->
<p class="text-2xl text-blue-300 mb-12">
```

## Fixing Broken Links

### Current Navigation Links
All internal section links in the navigation:
```html
<a href="#caracteristicas">Características</a>
<a href="#beneficios">Beneficios</a>
<a href="#faq">FAQ</a>
<a href="#contacto">Contacto</a>
```

### External Links
The main call-to-action button links to a form:
```html
<!-- Update this href with your form URL -->
<a href="https://form.jotform.com/250266352834053" class="inline-block bg-gradient-to-r...">
```

To update any link:
1. Locate the `<a>` tag
2. Change the `href` attribute value
3. For internal links, use `#section-id`
4. For external links, use the full URL including `https://`

## Linking Privacy and Terms Pages

### Footer Links Setup
Locate the legal section in the footer:
```html
<div>
    <h3 class="text-xl font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <!-- Update these href attributes -->
        <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors">Términos de Servicio</a></li>
        <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors">Política de Privacidad</a></li>
    </ul>
</div>
```

To add new policy pages:
1. Create `terms.html` and `privacy.html` in your root directory
2. Update the href attributes in the footer links
3. Ensure the new pages use consistent styling

Example privacy page link structure:
```html
<a href="privacy.html" class="text-gray-400 hover:text-white transition-colors">
    Política de Privacidad
</a>
```

## Troubleshooting

Common Issues and Solutions:

1. **Broken Internal Links**
   - Verify that section IDs match the href values
   - Check for typos in both the link and section ID
   - Ensure section IDs are unique

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Verify responsive classes (sm:, md:, lg:) are correct
   - Test on different screen sizes

3. **Gradient Text Not Showing**
   - Ensure all required classes are present:
     ```html
     bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent
     ```

4. **Navigation Menu Not Working**
   - Verify that section IDs exist in the page
   - Check that href values start with #
   - Ensure scroll-smooth class is on html element

Remember to:
- Always test changes in multiple browsers
- Maintain consistent spacing and indentation
- Back up files before making changes
- Test all links after updates

Need more help? Contact technical support or refer to the Tailwind CSS documentation.