## About Me

I teach high school physics in South Korea and study physics education at Kyung Hee University's Graduate School of Education.

My work includes:

- **Curriculum analysis:** For my master's thesis, I am mapping the physics involved in semiconductor wafer processing, metrology, and inspection to Korea's 2022 revised high school physics curriculum. The analysis uses 642 coded units from National Competency Standards (NCS) learning modules.
- **Open physics courseware:** I write and maintain [phyedu.net](https://phyedu.net/), with about 2,600 articles across 56 series and 59 interactive simulations. The material ranges from high school mechanics to graduate-level topics.
- **Teaching AI through physics:** My high school course introduces machine learning through ideas students encounter in the physics lab: least squares as a loss function, a ball rolling downhill as an analogy for gradient descent, and heat diffusion and its reversal as an introduction to diffusion models.
- **Machine learning experiments:** I study model training as a measurement problem. One project compares one-factor-at-a-time, Plackett–Burman, and full factorial designs across 156 training runs of a small CNN.

## Projects

| Project | Description | Built with |
| :--- | :--- | :--- |
| [phyedu.net](https://phyedu.net/) | Physics courseware for students who want to go beyond the textbook. Written in vanilla JavaScript, with automated checks for math rendering, figures, links, and accessibility that must pass before deployment. | Vanilla JS, KaTeX, Cloudflare Pages Functions, D1 |
| Simulations | 59 interactive browser labs, including a geological cross-section lab covering waves, resonance, heat, gravity, and electricity, and sunrise and sunset models based on public observatory data. | Canvas, SVG |
| Classroom tools | A live quiz tool with a question bank, calculation drills, a first-come, first-served seat picker, and a study planner. | Cloudflare D1, Firebase Realtime Database |
| Browser games | 20 small classroom games, including a top-down RPG, a four-lane rhythm game, real-time drawing games, and a typing trainer with sounds from 23 mechanical keyboard switches. Two games are also packaged as Android apps, and one has a Windows build. | Phaser 3, Canvas, Capacitor, Electron |
| Science shorts | Short physics explainers on [YouTube](https://www.youtube.com/@phyedunet) and [Instagram](https://www.instagram.com/phyedu_net/). Each episode uses a numerical physics simulation to generate every frame. The first 43 reels received 920,000 views in six days in August 2026. | Python, Pillow, FFmpeg, local TTS |
| AI course | 14 lessons and 14 PyTorch labs for high school students, from fitting a line to training a diffusion model. | Python, PyTorch |
| CNN sweep | 156 training runs on a binary classifier using 4,229 images, examining how the training budget changes whether regularization helps or hurts. | PyTorch |
| Exam paper builder | A script that generates exam papers with equations and figures in HWPML for the Hangul word processor. | Python, HWPML |

## Courseware

Each series follows a standard reference textbook and is written for self-study. Selected series are listed below, with article counts in parentheses.

| Area | Series |
| :--- | :--- |
| Core physics | Fluid dynamics (36), Nuclear physics (35), Plasma physics (31), Solid state physics (30), Nonlinear dynamics and chaos (30), Spintronics (24), Black holes (19) |
| Physics in other fields | Cooking (45), Climate (40), Magic tricks (37), Robotics (35), Medicine (34), Sound and musical instruments (29), Biophysics (25), Pharmacology (20) |
| Semiconductors | Semiconductor device physics (64), NCS learning module review (23) |
| Computing and AI | AI built by physics (28), Data analysis for physics (23), Deep learning (22), CUDA (20), From NAND to a computer (18) |
| Reading | Annotated classics (246 chapters across 27 books), Paper reviews (24) |

All 1,302 SVG figures and 3,045 tables have text descriptions. Automated checks block deployment if any descriptions are missing.

## Tools

JavaScript, Python, PyTorch, LaTeX, Cloudflare Workers and D1, Phaser 3, Unity

## Contact

- **Email:** [wldnjs1761@gmail.com](mailto:wldnjs1761@gmail.com)
- **Web:** [phyedu.net](https://phyedu.net/)
- **YouTube:** [@phyedunet](https://www.youtube.com/@phyedunet)
- **Instagram:** [@phyedu_net](https://www.instagram.com/phyedu_net/)
