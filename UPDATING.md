# Updating your website

You can make every change below directly on GitHub in your browser: open the file, click the pencil icon, edit, and click **Commit changes**. The site rebuilds and goes live about 2 minutes later (watch progress under the **Actions** tab).

## Where things live

| What | File |
|------|------|
| Homepage bio and research interests | `content/_index.md` |
| Name, tagline, email, LinkedIn | `hugo.yaml` (under `params:`) |
| Research page intro (dissertation, projects) | `content/research/_index.md` |
| Working papers and publications | `data/papers.yaml` |
| Reports | `data/reports.yaml` |
| Presentations | `data/presentations.yaml` |
| Teaching | `data/teaching.yaml` |
| Fellowships & awards | `data/awards.yaml` |
| Education | `data/education.yaml` |
| Policy & Practice page | `content/policy/_index.md` |
| Contact page | `content/contact/_index.md` |
| CV, paper PDFs | `static/files/` |
| Photo | `static/images/photo.jpg` |

## Add a new paper

1. Upload the PDF to `static/files/` (**Add file → Upload files**). Use a short name with no spaces, e.g. `sheinberg-2027-hip-use.pdf`.
2. Open `data/papers.yaml` and add an entry (copy an existing one). Published papers go in the list in reverse date order:

```yaml
- title: "Paper title"
  authors: ["Sheinberg, E.", "Leung, C.W."]
  year: 2027
  status: "published"
  venue: "Journal Name"
  citation: "12(3):456"
  pdf: "files/sheinberg-2027-hip-use.pdf"
  link: "https://doi.org/10.xxxx/xxxxx"
```

Your name (`Sheinberg, E.` or `Gahan, E.`) is bolded automatically.

## Mark a working paper as published

In `data/papers.yaml`, change `status: "under review"` to `status: "published"` and add `year`, `venue`, `citation`, `link`, and (optionally) `pdf`.

Status options: `published`, `accepted`, `revise and resubmit`, `under review`, `working paper`, `work in progress`.

## Add a teaching entry, award, or presentation

Open the matching file in `data/` and copy an existing entry to the top of the list.

## Update your bio

Edit `content/_index.md`. Plain text with blank lines between paragraphs. Wrap a phrase in `<span class="hl">...</span>` to show it in crimson.

## Update your CV

Upload the new PDF to `static/files/` named exactly `cv.pdf`, replacing the old one.

## Change your photo

Upload a new image named exactly `photo.jpg` to `static/images/`, replacing the old one. A portrait-orientation photo works best.

## Add a news section or blog

Ask your AI assistant — both are easy to add.

## Preview locally (optional)

```bash
brew install hugo
hugo server
```

Then open http://localhost:1313/esheinberg.github.io/.
