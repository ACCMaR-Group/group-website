# Hugo Content Management Guide

This guide explains how to efficiently add and manage content for your research group website.

## 1. Adding New Content

To add a new page or post, use the `hugo new` command from the root of your project. This will automatically include the necessary metadata (front matter).

### News / Blog Posts

```bash
hugo new news/title-of-your-post.md
```

### Publications

```bash
hugo new publications/paper-title.md
```

### People

```bash
hugo new people/new-member-name.md
```

## 2. Managing Drafts

New files created with `hugo new` usually have `draft: true` in the header.

- **To see drafts locally**: Run `hugo server -D`.
- **To publish**: Change to `draft: false` in the file's front matter.

## 3. Workflow Summary

Follow these steps when updating the site:

1. **Open Terminal**: Navigate to the project directory.
2. **Start Local Server**:

    ```bash
    hugo server -D
    ```

    View your site at: [http://localhost:1313/group-website/](http://localhost:1313/group-website/)
3. **Create/Edit Content**: Use `hugo new` and edit the resulting `.md` file.
4. **Save & Preview**: The local server will refresh automatically as you save.
5. **Commit & Push**:

    ```bash
    git add .
    git commit -m "Description of your changes"
    git push origin main
    ```

## 4. Tips for Images

When adding images to your posts, you can use the standard Markdown syntax or Hugo shortcodes.

- **Location**: Store new images in `static/media/`.
- **Reference**: In your Markdown, refer to them using:
  `{{< relURL "media/your-image.png" >}}`

## 5. Archetypes

If you want to customize the default "template" used for new publications or news, you can edit the files in the `archetypes/` directory. For example, editing `archetypes/default.md` changes the template for all new content.
