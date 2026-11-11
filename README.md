# Duecress 1.0 TEST
Native Android total weighted tardiness queue puzzle. Android8+ min26/target35. Package com.gg007.duecress.

## Rules
Arrange all six jobs A-F in a queue. Start at time 0, run one job at a time with no gaps and no interruption. TIME is duration, DUE is the desired finish time, and WT is penalty points per late time unit. FINISH is the running sum of durations through that job. Its PENALTY is max(0, FINISH minus DUE) times WT. Early and exactly-on-time jobs add zero; early jobs never subtract points. Minimize the sum of the six penalties. Tap one queue row then another to swap jobs; job duration, due time and weight move together. Tap a selected row again, or Undo, to cancel selection. CHECK QUEUE explicitly. Any minimum-penalty queue is accepted. Twelve original instances, each with one best order. Due times are soft targets, not feasibility restrictions. No jobs are omitted, and no money is involved.

## Download
https://mega.co.nz/#!gI9RVJib!Vst6IEhwsRI5qYFWziNluR3IE3tlMzXBBDFVBBto8DQ
{"url": "https://mega.co.nz/#!gI9RVJib!Vst6IEhwsRI5qYFWziNluR3IE3tlMzXBBDFVBBto8DQ", "bytes": 16878, "sha256": "abff72b13790ef74ca680d9c2eadb0afe84cad32924c7cef043a817e499e785e", "anonymous_bytes_exact": true}

## Checks
An independent lexicographic permutation oracle agrees with production subset dynamic programming on all 8,640 shipped orders and 2,000 random instances. Another 51,840 job finish-time and penalty calculations and all 432 row-pair swap/undo/cancel/reset cases pass. Twelve original queues have unique positive optima; alphabetical, earliest-due, shortest-duration and duration/weight orders are suboptimal on each. Empty, single, early, exactly on-time, late, zero-weight and out-of-bounds cases pass. Twelve actual queue-swap/CHECK optimum tap-solves, suboptimal-start rejection, selection cancel/undo/reset, solved lock/NEXT, levels/menu/privacy and saved palette/queue numbers pass. Twenty drawing previews inspected, not phone screenshots. Original signing certificate and GG007 icon bytes unchanged, no permissions. Anonymous APK bytes match. Phone runtime/performance/external-browser QA and full Git source commit remain incomplete. Signed TEST, not final or Play published.

## Functional difference
The live 246 studio descriptions and 803 legacy descriptions were reviewed. Slotcress selects a subset of fixed-time intervals; Assigncress chooses one worker/job pairing using fixed cell costs; Bandcress permutes graph nodes to minimize the largest linked slot gap. Duecress instead schedules every job sequentially and minimizes cumulative completion-dependent weighted tardiness. Changing an early job shifts later completion times and penalties. No fixed interval selection, fixed assignment matrix or minimax graph objective. Known single-machine weighted-tardiness adaptation, not a globally new algorithm. Twelve original seeded schedules, native implementation and two-row queue-swap interaction.

## Build and tests
JDK17, Android SDK35/build-tools35.0.0. python generate-levels.py reproduces levels.json. javac -d /tmp/prune-test src/com/gg007/duecress/Board.java BoardTest.java then java -cp /tmp/prune-test com.gg007.duecress.BoardTest. bash build.sh produces an aligned unsigned APK unless KEYSTORE_PATH and KEYSTORE_PASSWORD_FILE point to private signing material. No signing secret included. adapter/android is a Java2D drawing adapter used with DueAdapterTest.java, not an Android runtime.

## Privacy and branding
Duecress runs offline without accounts, ads, analytics, third-party SDKs or requested permissions. Palette, queue-number labels and solved-level marks stay in this app on your device. Clear app data or uninstall to remove them. The studio link opens your external browser.
GG007 icon/menu/studio https://ilanis-agent.github.io/gg-007-gaming/ and privacy.

## Preservation and publishing
Complete source/APK/exact cumulative247-card studio/publishing fragments privately preserved:
https://files.instinct.com/g4nrrbyatbmv-duecress-source-archive
https://github.com/iLanis-agent/duecress holds README only; full Git source pending. Four studio includes and Pages settings unchanged. Both sites verified separately.

## Rule sources
https://people.brunel.ac.uk/~mastjjb/jeb/orlib/wtinfo.html
https://cgi.di.uoa.gr/~sgk/papers/tardy-revised.pdf
https://fabiofurini.github.io/mip-modelling/scheduling-7/
https://metricgate.com/docs/weighted-tardiness-sequencing/
https://webdoc.sub.gwdg.de/ebook/serien/ah/UU-CS/2005-054.pdf
https://www.sciencedirect.com/science/article/abs/pii/S0360835208001265
