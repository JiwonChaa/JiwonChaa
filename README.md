**English** | [한국어](https://github.com/JiwonChaa/JiwonChaa/blob/main/README.ko.md)

## About Me

I teach high school physics in South Korea and study physics education at Kyung Hee University's Graduate School of Education.

My work includes:

- **Curriculum analysis:** For my master's thesis, I am mapping the physics involved in semiconductor wafer processing, metrology, and inspection to Korea's 2022 revised high school physics curriculum. The analysis uses 642 coded units from National Competency Standards (NCS) learning modules.
- **Open physics courseware:** I write and maintain [phyedu.net](https://phyedu.net/), with about 2,600 articles across 56 series and 59 interactive simulations. The material ranges from high school mechanics to graduate-level topics.
- **Teaching AI through physics:** My high school course introduces machine learning through ideas students encounter in the physics lab: least squares as a loss function, a ball rolling downhill as an analogy for gradient descent, and heat diffusion and its reversal as an introduction to diffusion models.
- **Machine learning experiments:** I study model training as a measurement problem. One project compares one-factor-at-a-time, Plackett–Burman, and full factorial designs across 156 training runs of a small CNN. Another runs a whole-brain model of the fruit fly connectome on a GPU and checks it spike for spike against a published model.
- **Student research and robotics:** I supervise student projects in physics and engineering, including a vibrational band gap on a string loaded with alternating masses, a code workflow for FIRST Tech Challenge (FTC) robots, and a ROS 2 autonomous robot.
- **Tools for school work:** I run an on-premises LLM server and build tools for finding research topics, diagnosing mock exam results, and preparing for admissions interviews.
- **Community:** I am an assistant manager of [물리 세계로의 즐거운 항해](https://cafe.naver.com/physvoyage) ("A Joyful Voyage into the World of Physics"), a physics community on Naver Cafe.

## Highlights

| Area | Work | Result |
| :--- | :--- | :--- |
| Courseware | [phyedu.net](https://phyedu.net/) | Includes about 2,600 articles across 56 series, with 59 interactive simulations. |
| Science shorts | Physics explainers on [YouTube](https://www.youtube.com/@phyedunet) and [Instagram](https://www.instagram.com/phyedu_net/) | Received 920,000 views for the first 43 reels in six days in August 2026. |
| Connectome | Whole-brain fruit fly model on a GPU | Models 139,255 neurons and matches the Brian2 model of Shiu et al. spike for spike. |
| Student research | Vibrational band gap on a loaded string | Predicts a forbidden band from 19.5 to 33.0 Hz among 11 normal modes. |
| Robotics | Active disturbance rejection control (ADRC) for FTC mechanisms | Showed a simulated error of about 0.2 under added load, compared with about 39 for PD control. |
| Local AI | On-premises LLM server with an RTX 5090 | Increased single-stream speed from 67.9 to 91.6 tokens per second. |
| Exam diagnosis | Mock exam diagnosis in which the server computes every number and the model writes only the sentences | Item accuracy in blind grading was 33/34 for a cloud model and 21/34 for a local model. |
| Interview data | Admissions interview question database | Contains about 37,500 questions from 225 universities. |

## Details

<details>
<summary><b>Physics courseware and media</b></summary>

<br>

| Project | Description | Built with |
| :--- | :--- | :--- |
| [phyedu.net](https://phyedu.net/) | Physics courseware for students who want to go beyond the textbook. Written in vanilla JavaScript, with automated checks for math rendering, figures, links, and accessibility that must pass before deployment. | Vanilla JS, KaTeX, Cloudflare Pages Functions, D1 |
| Simulations | 59 interactive browser labs, including a geological cross-section lab covering waves, resonance, heat, gravity, and electricity, and sunrise and sunset models based on public observatory data. | Canvas, SVG |
| Classroom tools | A live quiz tool with a question bank, calculation drills, a first-come, first-served seat picker, and a study planner. | Cloudflare D1, Firebase Realtime Database |
| Browser games | 20 small classroom games, including a top-down RPG, a four-lane rhythm game, real-time drawing games, and a typing trainer with sounds from 23 mechanical keyboard switches. Two games are also packaged as Android apps, and one has a Windows build. | Phaser 3, Canvas, Capacitor, Electron |
| Science shorts | Short physics explainers on [YouTube](https://www.youtube.com/@phyedunet) and [Instagram](https://www.instagram.com/phyedu_net/). Each episode uses a numerical physics simulation to generate every frame. | Python, Pillow, FFmpeg, local TTS |
| AI course | 14 lessons and 14 PyTorch labs for high school students, from fitting a line to training a diffusion model. | Python, PyTorch |
| Exam paper builder | A script that generates exam papers with equations and figures in HWPML for the Hangul word processor. | Python, HWPML |

Each courseware series follows a standard reference textbook and is written for self-study. Selected series are listed below, with article counts in parentheses.

| Area | Series |
| :--- | :--- |
| Core physics | Fluid dynamics (36), Nuclear physics (35), Plasma physics (31), Solid state physics (30), Nonlinear dynamics and chaos (30), Spintronics (24), Black holes (19) |
| Physics in other fields | Cooking (45), Climate (40), Magic tricks (37), Robotics (35), Medicine (34), Sound and musical instruments (29), Biophysics (25), Pharmacology (20) |
| Semiconductors | Semiconductor device physics (64), NCS learning module review (23) |
| Computing and AI | AI built by physics (28), Data analysis for physics (23), Deep learning (22), CUDA (20), From NAND to a computer (18) |
| Reading | Annotated classics (246 chapters across 27 books), Paper reviews (24) |

All 1,302 SVG figures and 3,045 tables have text descriptions. Automated checks block deployment if any descriptions are missing.

</details>

<details>
<summary><b>Machine learning and data</b></summary>

<br>

| Project | Description |
| :--- | :--- |
| Fly connectome explorer | Provides an environment for exploring the FlyWire connectome. Covers the adult female whole brain (FAFB v783, with 139,255 neurons and 54,492,922 synapses) and the male central nervous system (male CNS v1.0, with 166,700 neurons). Modules support neuron search, queries for upstream and downstream partners, connectivity matrices, shortest paths, synapse coordinates, and 3D views of skeletons and meshes. |
| Whole-brain simulation | Implements a leaky integrate-and-fire model of the whole brain on a GPU and verifies it spike for spike against the Brian2 model of Shiu et al. The model drives a NeuroMechFly body at 0.3 to 0.55 times real time. Stimulating sugar-sensing neurons causes proboscis extension. A looming stimulus triggers a jump through LPLC2 and the giant fiber, and MDN triggers backward walking. The body runs on flygym and MuJoCo. |
| Digit recognition with fly wiring | Uses a rate-based network with wiring fixed to the connectome and trains only the weights. On MNIST, it reached 96.55% accuracy with the real wiring and 96.87% with shuffled wiring. With the weights frozen, accuracy was 81.86% and 91.41%, respectively. The real wiring did not outperform the shuffled wiring, and the results are recorded as measured. |
| CNN sweep | Examines how the training budget affects whether regularization helps or hurts, using 156 training runs of a binary classifier on 4,229 images. Uses PyTorch. |
| Research topic tools | Provides an offline explorer for 39,804 past student research records in a single HTML file. Covers national science fair entries from 1949 to 2025, invention contest entries, and research reports from science-gifted programs. A duplicate-risk checker indexes 2,961 abstracts and treats a similarity of 0.32 to 0.42 as indicating existing research that differs from the proposal. The checker runs on Dify with bge-m3 embeddings. |
| Originex | Supports inquiry report writing and concept learning for high school students. Includes a collaborative editor with comments, equations, and revision history, and a five-step Socratic learning mode with a knowledge graph. Uses Next.js 16, Lexical, Yjs, MariaDB, and a local vLLM endpoint. |

</details>

<details>
<summary><b>Student research</b></summary>

<br>

I supervised these projects. Student names are omitted.

| Project | Description |
| :--- | :--- |
| Vibrational band gap on a loaded string | Tests whether a band gap arises from the mathematics of waves in a periodic structure, using a macroscopic system. Eleven 3D-printed masses, six of 7 g and five of 18 g, alternate at 5.2 cm intervals on a string under 7.84 N of tension. The small-angle approximation gives an equivalent spring constant of K = T/a = 150.8 N/m. The 11-degree-of-freedom eigenvalue problem predicts five lower modes and six upper modes separated by a forbidden band from 19.5 to 33.0 Hz. The gap of 13.5 Hz is 5.9 times the mean spacing of the other adjacent modes. The first three resonances were observed, and the upper branch remains to be measured. |
| Load limit of a cycloidal reducer | A student's 3D-printed cycloidal reducer broke at its output pins after testing. The follow-up study compares four infill patterns for the pins (3D honeycomb, truss, grid, and hollow) at a fixed density of 25%, adding water to a 700 g container in 100 g steps until the pins fail. |
| Truss and frame analysis | Analyzes a six-node symmetric truss with a 10 m bottom chord and an apex height of 8.7 m using the direct stiffness method. The model has 12 degrees of freedom, nine of them free. The same load is applied to a rigid frame for comparison, and equilibrium is checked for both structures using support reactions of 6 kN. |
| Failure probability of a structural member | Computes the probability P(R < S) with strength fixed at R ~ N(20, 4²) MPa, mean loads from 6 to 16 MPa, and coefficients of variation of 10%, 20%, and 30%. Compares the results with one million Monte Carlo trials. |
| Flow and heat simulations | Simulates flow around a folding drone wing at angles of attack of 5° and 7° and wind speeds of 40, 80, and 100 km/h. Includes an FFT script to find peak frequencies in the force history. Other projects cover wafer cooling by water, pipe flow at 1 to 10 m/s, wind load on buildings, and smoke spread for different fire locations in a house. |
| Drug release from alginate capsules | Provides guidance for a student interested in pharmacy. Includes counts of prior studies by topic, assessments of which experiments are feasible in a school laboratory, and a nine-week schedule. |

</details>

<details>
<summary><b>Robotics</b></summary>

<br>

| Project | Description | Built with |
| :--- | :--- | :--- |
| FTC code workflow | Converts a design exported from Fusion into a hardware specification in robot.yaml. The generated Java code must build, pass tests, and match the specification. The next stage deploys the code and tunes the robot through FTC Dashboard, and a mock Dashboard allows practice without a robot. Every command that moves the robot requires human confirmation. The workflow is not used during matches. Testing on a real Control Hub remains. | FTC SDK 12.0, Pedro Pathing 3.0, FTC Dashboard |
| ADRC for FTC mechanisms | Uses Subsystem and command code to control a lift (second order, position) and a flywheel (first order, velocity). Uses an extended state observer to estimate and compensate for disturbances from gravity, friction, and voltage sag. In simulation with added load, the ADRC error was about 0.2, compared with about 39 for PD control without disturbance estimation. Testing on hardware remains. | Java, FTCLib |
| R2-D2 autonomous robot | Built for display at a school festival. An ESP32 handles real-time control (motor PID, encoders, and IMU over micro-ROS), and a Raspberry Pi 4 handles SLAM, navigation, and effects. The twist_mux tool arbitrates between autonomous driving and gamepad control, with manual control taking priority. Eight packages, the firmware, and a Gazebo simulation have been drafted, and compilation and hardware testing remain. | ROS 2, micro-ROS, Nav2, Gazebo |
| Differential-drive AI robot | Uses a two-layer design with a Raspberry Pi 4 for perception, navigation, and speech, and a Pico for motor control. The binary serial protocol uses CRC16 and stops the motors if no command arrives within 200 ms. The plan has seven stages, each with completion criteria. | ROS 2, Raspberry Pi Pico |

</details>

<details>
<summary><b>Tools for school work</b></summary>

<br>

| Project | Description |
| :--- | :--- |
| Mock exam diagnosis tool | Computes expected scores, score losses, and appealing distractors on the server and uses the model only to write sentences. Sentences that fail verification are removed. For each wrong answer, the tool shows an item of the same type and a similar correct-answer rate from another exam, cropped from the original PDF. In blind grading, a cloud model achieved item accuracy of 33/34 and a local model 21/34. The local model often reversed the meaning of negatively worded questions, so statements about these questions now use fixed wording from the server. |
| Mock exam index | Stores mock exams and the CSAT from 2022 to 2026 in an item-level database. Includes questions, explanations, answers, points, correct-answer rates, and selection rates for each option. Records are complete for 159 of 165 papers. Uses SQLite. |
| Integrated science item book | Organizes 570 items from 27 Grade 10 achievement tests by unit, subunit, and difficulty. Includes a 20-item advanced mock exam checked by two independent solutions. |
| Admissions interview database | Contains about 37,500 questions from 225 universities, collected from universities' self-evaluation reports, official past questions, and applicant reports. In record-based interviews, 64% of questions ask about process and reasons, 16% about motivation, and 11% about concepts. None ask for derivations or calculations. The viewer is built with Next.js and SQLite and runs only locally. |
| Interview preparation booklets | Converts activities in a student's school record into a question-centered booklet. The pipeline extracts the activities, masks names and schools, organizes the material into eight areas, assigns priorities, creates activity cards, and assembles an A4 booklet. Every quotation is checked against the student's record. Scanned records are transcribed from page images to avoid OCR errors in quotations. |
| School record analyzer | Marks sentences that state exactly what the student did and sentences that state only intent or attitude directly in the original record. Evaluation runs on a local model after pseudonymization, and real names are restored only in the output. The parser handles spreadsheet exports in which several subjects share one cell and sentences break across pages. It processed 6,007 subject entries for 240 students with no unclassified or oversized entries. |
| Record draft pipeline | Uses code to make judgments and the model to write sentences. Includes an input quality check, generation with the text of the official recording guidelines, rule verification, fact verification, and automated detection of prohibited terms. Passed all 11 evaluation cases three times in a row. Uses Dify. |

</details>

<details>
<summary><b>Servers</b></summary>

<br>

| Project | Description | Built with |
| :--- | :--- | :--- |
| Local AI server | Runs on a Ryzen 9950X3D workstation with an RTX 5090 (32 GB). Requests pass through Cloudflare Tunnel and an nginx gateway to Dify for workflows and RAG, vLLM for inference, TEI with bge-m3 for embeddings, and SearXNG for search. | Dify, vLLM, TEI, SearXNG, LiteLLM |
| Inference tuning | Compares speculative decoding with one, two, and three predicted tokens. With two tokens, eight concurrent requests ran at 425 tokens per second, and three tokens reduced this to 288. Single-stream speed rose from 67.9 to 91.6 tokens per second, a 35% gain. Closing a wallpaper program raised throughput for eight concurrent requests from 422 to 483 tokens per second by reducing contention for GPU compute. | vLLM |
| Minecraft servers for students | Runs a Paper server with Geyser and Floodgate for Java and Bedrock players. Includes a custom chat plugin, three datapacks, backups every three hours, and two-way Discord chat. On a second server with 176 mods, 446 quests were translated into Korean on the server side, and 3,737 item and block names were translated using a 450-word dictionary. Names containing an unknown word are skipped. | Paper, Java |

</details>

<details>
<summary><b>Failures and fixes</b></summary>

<br>

- **Speed variation between restarts:** With identical settings, inference ran at either 21 or 93 tokens per second. The server sized its cache based on the VRAM available at startup, and the excess spilled into system RAM once desktop applications resumed. Lowering the GPU memory fraction from 0.92 to 0.87 resolved the problem.
- **Invented RAG answers:** The embedding container was the only one without a restart policy, so it stayed down after a reboot.
- **Invented citations with limited search results:** With only two search results, the model fabricated citations to fit the required format even under a strict prompt. Expanding the search resolved the problem, and all 29 citations across five test queries were then present in the search results.
- **Lenient grading without graded examples:** Removing human-graded examples from the evaluation harness raised the number of students given the top mark from 4 to 21. Negative criteria were added to recalibrate grading.
- **Disputes over grades:** The school record analyzer used grading scales, most recently with nine grades. The grades were removed, and the tool now marks the original text and reports counts and ratios.
- **Interview booklets above the required level:** The interview database showed that actual questions were at the level of high school textbooks, so the booklets were shortened from more than 100 pages to between 40 and 60 pages.
- **Fly simulation slowdown from a busy-wait loop:** A short polling loop in the real-time server made the simulation 50 times slower. The loop was replaced with an event-driven design.

</details>

## Tools

JavaScript, Python, PyTorch, Java, LaTeX, Cloudflare Workers and D1, Next.js, Phaser 3, Unity, ROS 2, Dify, vLLM, Fusion, Ansys Discovery

## Contact

- **Email:** [wldnjs1761@gmail.com](mailto:wldnjs1761@gmail.com)
- **Web:** [phyedu.net](https://phyedu.net/)
- **YouTube:** [@phyedunet](https://www.youtube.com/@phyedunet)
- **Instagram:** [@phyedu_net](https://www.instagram.com/phyedu_net/)
