# AI Use Note

I used ChatGPT to help scope the analysis, structure the notebook, draft Python code, and refine the explanation of findings.

One useful workflow was asking AI to translate the vague product question into a focused health-check artifact. It helped identify a practical comparison between model-reported confidence and human-facing outcomes such as output acceptance and review flags. AI also suggested session-weighted rate calculations and a focused visualization of the Reply Draft queue.

I did not accept the outputs without verification. I reviewed the source rows, ran each notebook cell, checked the calculated rates against the underlying counts, and confirmed that the notebook executed from top to bottom. I also decided to remove only the row explicitly labeled as a duplicate, retain the demo-account row as contextual evidence, and avoid imputing missing confidence or rating values. Finally, I treated the August 7 result as a signal for investigation rather than claiming the policy change or model caused the decline.
