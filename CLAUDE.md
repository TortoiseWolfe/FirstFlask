# CLAUDE.md - Working With FlaskFirst

## Build & Run Commands
- **Generate Project**: `bash FirstFlask.sh` - Creates House_Code directory with Flask app
- **Run App**: `cd House_Code && docker-compose up` - Start the Flask application
- **Stop App**: `cd House_Code && docker-compose down` - Stop running containers
- **View Logs**: `cd House_Code && docker-compose logs -f` - Follow container logs
- **Restart App**: `cd House_Code && docker-compose restart` - Restart after changes
- **Run Accessibility Tests**: `cd House_Code && ./test_accessibility.sh` - Test WCAG compliance
- **Run Unit Tests**: `cd House_Code && python -m pytest tests/test_accessibility.py -v` - Run unit tests

## Code Style Guidelines
- **SVG Assets**: Place SVG files in `_svg_assets/` directory with kebab-case filenames
- **Environment Variables**: Use `.env.example` as template; always use `TortoiseWolfe` for username
- **Repository Naming**: Use `The_House_that_Code_Built` as the standard repository name
- **GitHub Pages URL**: Follow format `https://TortoiseWolfe.github.io/The_House_that_Code_Built`
- **Python Imports**: Group standard library first, followed by third-party packages
- **HTML/CSS**: Follow BEM naming convention for CSS classes
- **JavaScript**: Use camelCase for variable/function names; organize code by feature
- **Error Handling**: Use try/except blocks when accessing files; provide informative fallbacks

## Accessibility Guidelines
- **ARIA Attributes**: All interactive elements must have proper ARIA roles and states
- **Keyboard Navigation**: All interactive elements must be keyboard accessible
- **Color Contrast**: Maintain a minimum contrast ratio of 4.5:1 for normal text, 3:1 for large text
- **Focus Management**: All interactive elements must have a visible focus state
- **Screen Reader Support**: Use proper semantic HTML and provide text alternatives
- **SVG Elements**: Add title elements and aria-label attributes to SVGs
- **Testing**: Run accessibility tests before each commit to ensure compliance

## Notes
- Docker environment is configured to mount SVG assets and environment variables
- GitHub Actions automatically handles deployment to GitHub Pages on push
- GitHub Actions includes automated accessibility testing with pa11y
- All SVG files should include proper title and desc elements for accessibility