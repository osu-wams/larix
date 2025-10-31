# Larix Theme

A Drupal 10 subtheme based on the [Bootstrap](https://www.drupal.org/project/bootstrap) base theme.

## Description

Larix is a custom Drupal 10 theme that extends the Bootstrap base theme, providing a foundation for building modern, responsive websites with Bootstrap's powerful framework.

## Requirements

- Drupal 9 or 10
- Bootstrap base theme (https://www.drupal.org/project/bootstrap)

## Installation

1. Download and install the Bootstrap base theme:
   ```
   composer require drupal/bootstrap
   ```

2. Place the Larix theme in your Drupal installation's themes directory:
   ```
   /themes/custom/larix
   ```

3. Enable the theme through the Drupal admin interface:
   - Navigate to Appearance (`/admin/appearance`)
   - Click "Install and set as default" for the Larix theme

   Or via Drush:
   ```
   drush theme:enable larix
   drush config:set system.theme default larix
   ```

## Structure

```
larix/
├── config/
│   ├── install/          # Default configuration
│   └── schema/           # Configuration schema
├── css/                  # Compiled CSS files
├── js/                   # JavaScript files
├── scss/                 # SCSS source files
├── templates/            # Twig template overrides
├── larix.info.yml       # Theme metadata
├── larix.libraries.yml  # Asset libraries
├── larix.theme          # Theme hook implementations
├── logo.svg             # Theme logo
└── README.md            # This file
```

## Customization

### CSS/SCSS

- Edit `scss/style.scss` for custom styles
- Compile SCSS to CSS in the `css/` directory
- Custom CSS is loaded via the `global-styling` library

### JavaScript

- Add custom JavaScript in `js/larix.js`
- JavaScript behaviors follow Drupal standards

### Templates

- Override Bootstrap or Drupal core templates by placing them in the `templates/` directory
- Follow Drupal's template naming conventions

### Theme Settings

- Configure theme settings at `/admin/appearance/settings/larix`
- Custom settings can be added via `larix_form_system_theme_settings_alter()` in `larix.theme`

## Development

### Compiling SCSS

If you modify SCSS files, compile them to CSS:

```bash
# Using sass (install via npm or gem)
sass scss/style.scss css/style.css
```

### Cache Clearing

After making changes, clear Drupal's cache:

```bash
drush cache:rebuild
```

## Support

For issues, feature requests, or contributions, please use the project's issue queue.

## License

This theme is licensed under the GPL v2 license. See LICENSE file for details.
