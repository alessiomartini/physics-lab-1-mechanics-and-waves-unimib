# Physics Laboratory I — Experiments, Data and Reports (UniMiB)

Working archive for *Laboratorio di Fisica I*, BSc in Physics, Università degli
Studi di Milano-Bicocca, academic year **2020/2021** — Alessio Martini, with
lab partner Matthew Maisano.

This is the complete record of the course as it was actually run: raw
measurements as they came off the instruments, the spreadsheets used to reduce
them, the LaTeX reports written from them, and the exam papers. Because
2020/2021 was a remote-teaching year, several experiments were performed **at
home** with a smartphone as the measuring instrument (the
[phyphox](https://phyphox.org/) app), which is why some datasets are exported
sensor traces rather than lab-bench readings.

Documents and file names are in Italian.

## The experiments

| Experiment | Files | What is measured |
| --- | --- | --- |
| **Introductory: gravity** | `ESPERIENZA INTRODUTTIVA Gravita.docx` / `.pdf`, `Pendolo - Esperienza Introduttiva.xlsx` | $g$ from the period of a simple pendulum — the first experiment of the course, used to introduce uncertainty propagation |
| **Cavendish balance** | `Cavendish/`, `Cavendish_2018.pdf` | The gravitational constant $G$ from the torsion balance. `Cavendish/Bilancia di Cavendish - Ale.pdf` is the finished report; alongside it are the working screenshots and the plots of the sensitivity of $G$ to the period $T$ and to the calibration constant $c$ (`G_deriv_risp_T.PNG`, `G_deriv_risp_c.PNG`). `Cavendish_2018.pdf` is the reference write-up from a previous year |
| **Coulomb balance** | `Coulomb/`, `Bilancia di Coulomb.xlsx`, `coulomb_15.pdf` | The inverse-square law of electrostatics: force versus charge and force versus separation (`forza carica.png`, `forza raggio.png`), with the data reduction in the spreadsheet |
| **Springs** | `Molle - da Casa.xlsx` | Hooke's law measured at home ("da Casa") — spring constant from load versus extension |
| **Bouncing ball, restitution coefficient** | `Pallina coefficiente di restituzione/` | Eleven `Data from phyphox` exports — Excel workbooks saved without an extension, columns *Start (s) / Stop (s) / Difference (s)*, produced by phyphox's acoustic stopwatch. The phone's microphone timestamps each impact of a bouncing ball, and the coefficient of restitution follows from how the intervals between bounces shrink |
| **Acoustic tube** | `Tubo Acustico (80esima misura).xlsx` | Standing waves in a tube — resonance frequencies, and from them the speed of sound |
| **Forced and damped oscillator** | `Oscillatore Forz-Smorz/` | Screenshots of the acquisition for a driven damped oscillator |

## Reports and templates

- **`lab_report_1/`** — a LaTeX lab-report template (`lab_report_1.tex` +
  `sample.bib`), still carrying its upstream demo content (*"Determination of the
  Atomic Weight of Magnesium"*) with the section skeleton the course expected:
  Objective, Experimental Data, Sample Calculation, Results and Conclusions,
  Discussion of Experimental Uncertainty, Answers to Definitions. Start from
  here when writing a new report. `lab_report_1.zip` is the same thing as
  downloaded.
- **`18b_relazione_esempio_misurag/`** — the course's **example report on
  measuring $g$**, kept as a model of what a finished write-up should look like.
  The `.tex` is a machine conversion of the PDF (absolutely-positioned boxes and
  generated colour definitions, with a hard-coded `\graphicspath` pointing at
  the conversion service), so it is readable as a document but not usefully
  editable as source. Its `.history/` subfolder — timestamped snapshots written
  automatically by the VS Code *Local History* extension — contains a blank
  Overleaf skeleton for the Cavendish report, still filled with the default
  placeholder text; the real Cavendish write-up is the PDF under `Cavendish/`.

## Exams and study material

- `Scritto_Feb2021.pdf`, `Scritto_Giu2021_finale.pdf` — the February and June
  2021 written exam papers.
- `Appunti Nick/` — 58 photographs of a coursemate's handwritten lecture notes,
  shared over WhatsApp in February 2021 (hence the `IMG-2021…-WA…` names).

## Notes for anyone opening this repository

- **`PASCO Capstone Files - Shortcut.lnk`** is a Windows shortcut to a local
  folder on the machine used at the time. It points nowhere on any other
  computer — the PASCO Capstone acquisition files it referenced were never
  committed.
- The `desktop.ini` files are Windows folder-metadata leftovers and can be
  ignored.
- The `.xlsx` spreadsheets are where the data reduction happens: raw readings,
  propagated uncertainties, and the fits that produce the final numbers.

## Related repository

- [`physics_lab_2_unimib`](https://github.com/alessiomartini/physics_lab_2_unimib)
  — the second-year laboratory course.
