# Templates Directory

Place Twig template overrides in this directory.

## Usage

To override a template:

1. Copy the template from the Bootstrap base theme or Drupal core
2. Place it in this directory (maintaining subdirectory structure if needed)
3. Modify the template as needed
4. Clear cache: `drush cache:rebuild`

## Common Templates

- `page.html.twig` - Overall page structure
- `node.html.twig` - Node display
- `block.html.twig` - Block display
- `region.html.twig` - Region containers

## Template Suggestions

Drupal allows specific template suggestions:
- `page--front.html.twig` - Front page only
- `node--article.html.twig` - Article content type only
- `block--system-branding-block.html.twig` - Specific block

Refer to Drupal documentation for complete template naming conventions.
