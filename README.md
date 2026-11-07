# DeCAR — Detect, Correlate, Analyze, Report

**A perception system tells you what each camera saw. DeCAR tells you what happened.**

## The problem it exists for

Modern camera software is good at perception and blind to continuity. It will tell you that
camera 3 saw a person at 21:04 and that camera 7 saw a person at 21:06 — but not that it was the
same person, walking from the driveway to the side gate. Every event stands alone. The
correlation is left to whoever is scrolling the timeline at midnight.

DeCAR is the layer that does that work. It takes the per-event perceptions your cameras already
produce and correlates them into persistent **entities**, **relationships** and **activities**
that span cameras and time, so the question you can ask moves from *"show me clips from the last
hour"* to *"what happened last night?"*.

It **runs no perception of its own** — no object detector, no face matcher, no plate reader. It
orchestrates the ones you already have and remembers what they said.

## Who it is for

Someone self-hosting their own cameras who already has detection working — Frigate, or any system
that can emit a detection with a camera, a time and a bounding box — and who wants memory and
reasoning on top of it, on their own hardware.

Everything runs on the property. There is no account, no cloud service and no per-camera fee, and
nothing leaves the premises unless you point an analytics connector at an external model endpoint
yourself. Do that and the core will not start the connector until you have acknowledged the
disclosure, with the acknowledgment recorded against the endpoint it was given for.

## See the console without installing anything

[`demo/decar-console-demo.html`](demo/decar-console-demo.html) is a single self-contained page
showing the whole management console — Timeline, Detections, Associations, Watchlists and Review,
plus the Policies, Normalization, Connectors, Analysis, Cameras and Matching health sections of
Settings (and Users, which is a nav item rather than a screen). Open it directly from disk: no
server, no build step, no network, and no external reference of any kind.

It is a **demo, not the product.** Everything in it is fixed sample data, and it says so in a
banner you cannot scroll past.
