# EdgeSS: Sensor Synthesis at the Edge 

This repository serves as the central collaboration and documentation hub for the **EdgeSS (Sensor Synthesis at the Edge: Scalable Environmental Insights from Real-time Data)** project.

EdgeSS brings together environmental scientists, data scientists, AI researchers, and cyberinfrastructure experts to develop scalable approaches for integrating real-time environmental sensor data, edge computing, and artificial intelligence. The project focuses on advancing environmental monitoring and decision-making through distributed sensing systems and interoperable data workflows.

The repository supports project coordination, technical documentation, working group activities, meeting materials, and public-facing project communication through an automatically generated website.

## Project Objectives

EdgeSS is organized around three environmental challenge areas:

* **Invasive Species Monitoring** – Tracking and understanding the spread of invasive organisms such as the Spotted Lanternfly using distributed sensing networks and AI-enabled detection systems.
* **Forest Disturbance and Ecosystem Response** – Investigating how wildfire, drought, insects, and disease influence vegetation dynamics, phenology, and ecological resilience.
* **Air Quality and Environmental Health** – Examining spatial and temporal patterns in air pollution using real-time environmental sensing and edge-based analytics.

The project leverages emerging cyberinfrastructure, including smart sensors, edge computing platforms, environmental observatories, and AI-driven data processing pipelines to generate actionable environmental insights at scale.

---

## Repository Structure

This repository is organized as a connected system that supports both project development and public dissemination.

```text
.
├── README.md              # Project overview and repository guidance
├── mkdocs.yml             # Website configuration and navigation
├── docs/                  # Public-facing project website content
├── scripts/               # Site utilities and automation scripts
├── templates/             # Meeting notes and project templates
├── containers/            # Development and deployment environments
└── project folders        # Research materials, workflows, data products, and analyses
```

### Documentation Layer

The `docs/` directory contains the source content for the EdgeSS website. Content in this directory is automatically rendered into a public project website using MkDocs.

Examples include:

* Project overview and goals
* Working group information
* Meeting notes and project updates
* Technical documentation
* Training materials and resources
* Project deliverables and outputs

### Research and Development Layer

Additional project folders contain the scientific and technical work that supports EdgeSS activities, including:

* Data workflows
* Analysis notebooks
* Edge computing experiments
* Sensor integration documentation
* AI and machine learning workflows
* Figures, reports, and deliverables

---

## Frequently Updated Files

Common files and locations that project contributors may edit include:

* `docs/index.md` – Project homepage
* `docs/work-plan.md` – Project roadmap, milestones, and meeting tracking
* `docs/how-this-group-works.md` – Collaboration guidelines and team practices
* `docs/esiil-resources/` – Shared ESIIL resources and training materials
* `docs/instructions/` – Contributor and GitHub guidance
* `docs/resources/` – Reference materials and supporting documentation

---

## Local Development

Install dependencies and start a local preview of the website:

```bash
pip install -r requirements.txt
python scripts/generate_image_slots.py
python scripts/site_health.py
mkdocs serve
```

The site will be available locally and automatically update as documentation changes are made.

---

## Building the Site

Generate a production build of the website:

```bash
python scripts/generate_image_slots.py
python scripts/site_health.py
mkdocs build --strict --clean
```

---

## Managing Images and Visual Assets

The website uses semantic image slots to simplify updating project visuals without modifying Markdown references.

### Homepage and Shared Images

1. Navigate to the appropriate folder in `docs/assets/images/slots/`
2. Replace the existing image with a new file
3. Run:

```bash
python scripts/generate_image_slots.py
```

4. Commit both the image and regenerated references

### Process Galleries

Process galleries automatically render content placed in:

```text
docs/assets/images/process/
```

Supported content includes:

* Images (`png`, `jpg`, `jpeg`, `webp`, `svg`)
* Deliverables (`pdf`, `html`, `csv`, `xlsx`, `docx`, `pptx`)

Captions may be added using a `captions.txt` file.

---

## Site Health Checks

A site health report is generated during each build to help identify:

* Missing files
* Broken references
* Placeholder content
* Navigation issues
* Incomplete template sections

Warnings do not prevent publication but help maintain documentation quality.

---

## Automated Publishing

The EdgeSS website is automatically built and deployed through GitHub Actions whenever changes are merged into the repository.

This allows project documentation, meeting materials, and public-facing resources to remain synchronized with ongoing project development and collaboration activities.

