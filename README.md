# Jekyll GitHub Pages Scaffolding

A minimal scaffolding project for running Jekyll sites locally using Docker, designed for GitHub Pages deployment.

## Description

This project provides a quick-start template for Jekyll-based GitHub Pages sites. It uses Docker to ensure a consistent development environment without requiring local Jekyll/Ruby installation.

## Dependencies

- [Docker](https://www.docker.com/get-started) (includes Docker Compose V2)

## Quick Start

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd ghpages-scaffolding
   ```

2. **Start the Jekyll server**
   ```bash
   docker compose up
   ```

3. **View your site**

   Open your browser and navigate to: `http://localhost:4000`

4. **Stop the server**

   Press `Ctrl+C` in the terminal, or run:
   ```bash
   docker compose down
   ```

## Project Structure

```
.
├── _config.yml          # Jekyll configuration file
├── docker-compose.yml   # Docker Compose configuration
├── .gitignore          # Git ignore rules
└── README.md           # This file
```

## Configuration

Edit `_config.yml` to customize your site:

- **title**: Your site title
- **email**: Your contact email (currently commented out)
- **description**: Site description
- **baseurl**: Base URL path (for subpath deployments)
- **url**: Full site URL

### Current Settings

- Jekyll version: 4.2.0
- Markdown processor: kramdown
- Permalink style: none
- Server port: 4000

## Deployment to GitHub Pages

1. **Configure your repository**
   - Update the `url` and `baseurl` in `_config.yml`
   - Set `url` to `https://<username>.github.io`
   - Set `baseurl` to `/<repository-name>` (if using a project page)

2. **Push to GitHub**
   ```bash
   git add .
   git commit -m "Initial Jekyll site"
   git push origin main
   ```

3. **Enable GitHub Pages**
   - Go to repository Settings > Pages
   - Select your source branch (usually `main`)
   - Your site will be published at `https://<username>.github.io/<repository-name>`

## Generated Files

The following directories are auto-generated and ignored by git:

- `_site/` - Generated static site files
- `.jekyll-cache/` - Jekyll cache for faster builds

## Useful Commands

- **Rebuild the site**: Changes to most files are auto-detected, but restart the server after modifying `_config.yml`
- **Clean build**: Remove the containers and rebuild
  ```bash
  docker compose down
  docker compose up --build
  ```

## Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Jekyll Themes](https://jekyllrb.com/docs/themes/)

## License

This scaffolding is provided as-is for use in your projects.

## Author

By Tom DeForest
