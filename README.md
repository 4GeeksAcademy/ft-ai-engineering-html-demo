# HTML Hello

The most basic boilerplate for any 4Geeks Academy student, start your very first website from scratch.

> There is a video tutorial on [how to use this template to create your very first website here](https://youtu.be/dfbDCMu_p-0).

## What to do next?

Create an `index.html` file with the [basic HTML structure](http://4geeks.com/lesson/what-is-html-learn-html#page-structure) and see it live by running a web-server using the following command:

```bash
$ pip3 install flask && python3 server.py
```

- You can create as many HTML files as you want.
- You can also create CSS files and import them into your website using a `<link>` tag placed between the `<head></head>` tags, like this:

```html
<head>
  ...
  <link rel="stylesheet" type="text/css" href="styles.css" />
  ...
</head>
```

- If you want to use Tailwind CSS, add it optionally via the official Tailwind CSS v4 CDN inside the same `<head>`:

```html
<head>
  ...
  <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
  <link rel="stylesheet" type="text/css" href="styles.css" />
  ...
</head>
```

## Project Stages

This repository now includes three learning stages, each with its own HTML and CSS:

- `stage-1-semantic-bem/index.html` + `stage-1-semantic-bem/styles.css`
- `stage-2-tailwind/index.html` + `stage-2-tailwind/styles.css`
- `stage-3-design-components/index.html` + `stage-3-design-components/styles.css`

The root `index.html` links to every stage so students can compare approaches side by side.

## GitHub Pages Hosting

This repository includes a GitHub Pages workflow in `.github/workflows/pages.yml`.

After enabling Pages in repository settings, the site will be published from the workflow run and available at:

`https://4geeksacademy.github.io/ft-ai-engineering-html-demo/`

If your fork has a different owner or repository name, update the URL pattern accordingly:

`https://<owner>.github.io/<repo>/`

### Recommended GitHub Pages Settings

1. Go to repository Settings -> Pages.
2. Set Source to `GitHub Actions`.
3. Push to the deployment branch (`main` by default) to publish updates.

## Known Issues

- Dark mode toggle troubleshooting notes are documented in [TODO.md](TODO.md).

### Contributors

This template was built as part of the [Full Stack Developer course](https://4geeksacademy.com/us/coding-bootcamps/part-time-full-stack-developer) at [4Geeks Academy Coding Bootcamp](https://4geeksacademy.com/us/coding-bootcamp) by [Alejandro Sanchez](https://twitter.com/alesanchezr) and [many other contributors](https://github.com/4GeeksAcademy/html-hello/graphs/contributors).

You can find other templates and resources like this at the [school's GitHub page](https://github.com/4geeksacademy/).
