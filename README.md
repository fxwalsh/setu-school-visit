# Ard Scoil na Mara School Visit

Tutors course source containing one topic, one talk, and two versions of the Charting Champions lab.

## Presentation

The supplied presentation and its PDF export are in `topic-01-setu-programmes/talk-01-setu-programmes/`. Tutors embeds the PDF in the talk page; the original PowerPoint is retained as a source file.

## Build and run locally

From this folder, build the local HTML version with Deno:

```powershell
deno run -A jsr:@tutors/tutors-lite
```

Then serve the generated `html` folder locally:

```powershell
deno run --allow-net --allow-read=html jsr:@std/http/file-server html --port 8000
```

Open <http://localhost:8000/>. Stop the server with Ctrl+C. The first run may download the Deno packages from JSR.

Card artwork uses Iconify SVG icons configured in `properties.yaml` and the topic, talk, and lab front matter. The icons are loaded from Iconify, so an internet connection is needed to display them.

## Course structure

- Course: Ard Scoil na Mara School Visit
- Topic: SETU Programmes
- Talk: SETU Programmes (PDF slides)
- Lab: Charting Champions (eight-step Markdown version)
- Notebook: Charting Champions (Jupyter version)

The original lab uses the Tutors `book-*` convention and ordered `NN.Short-title.md` files. The notebook version is a separate `notebook-*` resource; it keeps its CSV examples inline so it can run in a browser notebook without local file uploads. Downloadable resources for the original lab are in its `archives` folder. Use your existing Tutors publishing workflow after completing the talk. No deployment URL or repository was supplied.

## Session preparation

Allow approximately 60–75 minutes for either lab version. Work in pairs and swap keyboard roles halfway through. For the original lab, download and extract the starter ZIP and install Python 3 and Pygal on each machine. The notebook version installs Pygal in Tutors' browser Python runtime, so internet access is needed on its first run. Test SVG opening on the school computers. Internet access is also needed for the Iconify icons and may be needed for chart hover/legend interactions; the static chart remains useful without them.

The local route is self-contained after installing Pygal. Historical medal values are a five-row extract from the original teaching example, not current Olympic totals. Population/GDP practice files use explicitly fictional countries and figures. For the original real-world investigation, use the data supplied by the linked Raspberry Pi project and inspect its dates, units and definitions before drawing conclusions.

## Attribution

Lab adapted from Raspberry Pi Foundation, [Charting champions](https://projects.raspberrypi.org/en/projects/charting-champions/0), under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/). An accessible [Code Club PDF edition](https://assets.codeclubau.org/assets/Charting-champions.pdf) was used to read the project. Changes include Tutors formatting, school-session prompts, local SVG output, shorter historical sample, fictional comparison data, and debugging support. Adapted lab text and accompanying examples are distributed under CC BY-SA 4.0. The SETU presentation remains subject to its own rights and is not covered by this licence.
