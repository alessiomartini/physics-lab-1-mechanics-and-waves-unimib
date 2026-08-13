# Physics Laboratory I — Experiments, Data and Reports (UniMiB)

Working archive for *Laboratorio di Fisica I*, BSc in Physics, Università degli
Studi di Milano-Bicocca, academic year **2020/2021** — Alessio Martini, with
lab partner Matthew Maisano.

This is the complete record of the course as it was actually run: raw
measurements as they came off the instruments, the spreadsheets used to reduce
them, the finished reports written from them, and the exam papers. Because
2020/2021 was a remote-teaching year, several experiments were performed **at
home** with a smartphone as the measuring instrument (the
[phyphox](https://phyphox.org/) app), which is why some datasets are exported
sensor traces rather than lab-bench readings.

Documents and file names are in Italian.

## The reports

Three finished write-ups, by **Alessio Martini and Matthew Maisano** (instructor:
ACM Bulla), each about nine pages. These are the deliverables of the course; the
spreadsheets and raw data listed further down are the working material behind
them.

### `Bilancia_di_Cavendish.pdf` — measuring the gravitational constant

The torsion balance, measured in three steps: the **torsion constant** of the
wire, the **rotation angle** $\theta$ of the balance, and from them $G$. The
report derives a closed form for $G$ in terms of directly measured quantities
only,

$$G = \frac{2\pi^2\left(d^2 + \tfrac{2}{5}r^2\right)\arctan\!\left(\tfrac{t}{2L}\right)}{dM\left(\tfrac{1}{b^2} - \tfrac{b}{b^2 + 4d^2}\right)T^2}$$

which is the expanded version of the more intuitive $G = \kappa\theta / [\,2dmM(\dots)\,]$.

$$G = (6.62 \pm 0.28)\times 10^{-11}\ \mathrm{N\,m^2\,kg^{-2}}$$

— 0.8%, or **0.18σ**, from the accepted value. The report closes by identifying
where the uncertainty actually comes from: the dominant contribution is the
measurement of $t$, the distance between the two equilibrium positions on the
screen, so that is the first thing to improve.

*Riflessioni*: how to measure the period of a **damped** oscillation correctly,
and the relation between the distances and the torsion angle.

### `Bilancia_di_Coulomb.pdf` — the electrostatic force law

Angle as a function of separation, then as a function of charge, then the
permittivity of free space from the torsion constant.

Both dependences in Coulomb's law are confirmed separately — $F$ against $1/r^2$
is linear, while $F$ against $Q$ is not, going as the *product* of the two
charges. The extracted permittivity is

$$\epsilon_0 = (7.5 \pm 0.34)\times 10^{-12}$$

which sits **3.7σ** from the accepted value, and the report says so plainly
rather than hiding it, attributing the gap to uncertainties that were not
accounted for in the measurement chain — the weight force among them.

### `Relazione_Esperienza_Onde_Acustiche.pdf` — sound waves in an acoustic tube

A plexiglass tube, a speaker at one end, a microphone inside, an oscilloscope
reading both signals; the resonance frequency is studied as a function of tube
length, with the **end correction** applied ($L + 0.8D$ for a tube open at both
ends, $L + 0.4D$ for one closed at one end — and the report verifies that the
two geometries obey genuinely different relations, $n\lambda/2$ against
$(2n-1)\lambda/4$).

The tube is then filled with two other gases, giving the speed of sound in each:

| Gas | Speed of sound |
| --- | --- |
| Air | $341.69 \pm 0.56$ m/s |
| Argon | $319.06 \pm 0.42$ m/s |
| Krypton | $224.26 \pm 0.16$ m/s |

A separate measurement using square waves provides an independent check.

## The experiments and their raw data

| Experiment | Files | What is measured |
| --- | --- | --- |
| **Introductory: gravity** | `ESPERIENZA INTRODUTTIVA Gravita.docx` / `.pdf`, `Pendolo - Esperienza Introduttiva.xlsx` | $g$ from the period of a simple pendulum — the first experiment of the course, used to introduce uncertainty propagation |
| **Cavendish balance** | `Cavendish/`, `Cavendish_2018.pdf` | `Cavendish/Bilancia di Cavendish - Ale.pdf` is not a report but a two-page printout of the data reduction: the moment-of-inertia and oscillation-period calculations, with the two straight-line fits over even and odd half-periods. Beside it are the working screenshots and the plots of the sensitivity of $G$ to the period $T$ and to the calibration constant $c$ (`G_deriv_risp_T.PNG`, `G_deriv_risp_c.PNG`). `Cavendish_2018.pdf` is the **instructor's lab manual** (M. Calvi, 2018): apparatus description and procedure, including the warning not to touch the suspension wire |
| **Coulomb balance** | `Coulomb/`, `Bilancia di Coulomb.xlsx`, `coulomb_15.pdf` | `coulomb_15.pdf` is the **raw data sheet for group 15**: angle against separation at 6000 V, then against voltage, with the stated instrument precisions (1 mm on the graduated scale, 1° on the goniometer, 100 V steps on the generator, 3.8 cm sphere diameter). `Coulomb/` holds the resulting plots (`forza carica.png`, `forza raggio.png`) and the spreadsheet the reduction was done in |
| **Springs** | `Molle - da Casa.xlsx` | Hooke's law measured at home ("da Casa") — spring constant from load versus extension |
| **Bouncing ball, restitution coefficient** | `Pallina coefficiente di restituzione/` | Eleven `Data from phyphox` exports — Excel workbooks saved without an extension, columns *Start (s) / Stop (s) / Difference (s)*, produced by phyphox's acoustic stopwatch. The phone's microphone timestamps each impact of a bouncing ball, and the coefficient of restitution follows from how the intervals between bounces shrink |
| **Acoustic tube** | `Tubo Acustico (80esima misura).xlsx` | The measurement series behind `Relazione_Esperienza_Onde_Acustiche.pdf` — resonance frequencies against tube length |
| **Forced and damped oscillator** | `Oscillatore Forz-Smorz/` | Screenshots of the acquisition for a driven damped oscillator |

## Templates and example reports

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
  placeholder text; the finished Cavendish write-up is `Bilancia_di_Cavendish.pdf`
  at the repository root.

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
  — the second-year laboratory course: six reports on circuits (Ohm's law and
  diodes, RC/RL/RLC transients, resonance) and on waves and optics
  (interferometry, microwaves, spectrometry).
