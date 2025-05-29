# Personal Blog

This is a simple personal blog built using Jekyll. It serves as a platform to share thoughts, ideas, and experiences through blog posts.

## Project Structure

- **_config.yml**: Jekyll configuration file containing basic settings like title, description, and author information.
- **_layouts**: Contains layout files for different types of pages.
  - **default.html**: Default layout for all pages.
  - **post.html**: Layout specifically for blog posts.
  - **page.html**: Layout for regular pages.
- **_includes**: Contains reusable components for the site.
  - **header.html**: Header section with navigation and site title.
  - **footer.html**: Footer section with copyright and additional links.
  - **navigation.html**: Navigation menu for the site.
- **_posts**: Directory for blog posts.
  - **2024-01-01-welcome-to-my-blog.md**: First blog post.
  - **2024-01-02-second-post.md**: Second blog post.
- **_sass**: Contains Sass files for styling.
  - **_base.scss**: Base styles for the site.
  - **_layout.scss**: Layout styles for the site.
  - **_syntax-highlighting.scss**: Styles for code syntax highlighting.
- **assets**: Contains static assets like CSS and JavaScript files.
  - **css/main.scss**: Main stylesheet for the site.
  - **js/main.js**: Main JavaScript file for site interactions.
- **about.md**: About page with personal information or site introduction.
- **index.html**: Homepage with welcome message and links to latest posts.
- **Gemfile**: Bundler configuration file listing required Ruby gem dependencies.

## Installation

To set up this blog locally, follow these steps:

1. Clone the repository:
   ```
   git clone <repository-url>
   cd personal-blog
   ```

2. Install dependencies:
   ```
   bundle install
   ```

3. Serve the blog locally:
   ```
   bundle exec jekyll serve
   ```

4. Open your browser and navigate to `http://localhost:4000` to view the blog.

## Usage

You can create new blog posts by adding Markdown files to the `_posts` directory. Make sure to follow the naming convention `YYYY-MM-DD-title.md` for the files. Each post should include the necessary front matter at the top of the file.

## License

This project is licensed under the MIT License. Feel free to use and modify it as you wish.