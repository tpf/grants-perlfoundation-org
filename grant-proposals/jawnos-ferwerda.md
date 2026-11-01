# Grant Proposal: Documenting and stabilising JawnOS, a 138,000-line Perl application

## Grantee: Jonathan Ferwerda

Warwick, Ontario, Canada · jonathan.ferwerda@outlook.com · https://github.com/jonathanferwerda/jawnos · jawnos.ca

## Synopsis

JawnOS is a personal operating environment written in Perl and Mojolicious: a browser-delivered
desktop with files, calendar, mail, notes, chat and SMS, a music player and recorder, invoicing, a
double-entry ledger with income statements, warehouse stock moves with coordinates on measured maps,
and four local agents. All state lives in one encrypted SQLite file. It runs on a phone under Termux,
synchronises between machines with no central server, and speaks to ESP32 and RP2040 hardware over
Bluetooth, including a custom wake word.

It has been in continuous development for four years. Three years and eleven months of it were written
by hand; agentic tooling entered the workflow only in the final month, and the architecture predates
it. Counted on 1 November 2026, it is more than 138,000 lines of Perl, plus 23,000 lines of
Mojolicious templates. It is BSD-2 and pre-alpha.

Most Perl in production is glue. Large Perl applications exist, but almost nobody writes down how they
are built, so the patterns are relearned privately by every generation. JawnOS is a counter-example,
and this grant turns it into documentation the community can reuse: one Mojolicious application across
several workers, with Sereal over Unix sockets between them; Minion for background jobs; one big
record table with a small, deliberate set of satellite tables; a mesh that synchronises without a
central authority and resolves deletions with tombstones; and an application that can watch its own
error log and propose a patch, then compile and ship it under the same discipline a person uses.

The grant funds four artefacts: an architecture guide, six signed monthly releases, an automated test
suite for the ledger and the mesh, and one conference talk with a written version. These are
documentation and release engineering, not user support: the deliverables are dated, self-directed,
and published under BSD-2 with the rest of the tree.

## Grant Deliverables

* **An architecture guide**, 40–60 pages in twelve chapters, published in the repository under BSD-2.
  It covers the browser desktop and what it constrains; the record table and its satellites; the
  ledger inside a record table; the worker topology; Sereal over Unix sockets; Minion; the sync mesh
  and its tombstones; the security model; the hardware layer; the agents; testing a system with no API
  boundary; and a final chapter on what I would do differently.
* **Six signed monthly releases**, each tagged, soaked seven days, with a changelog, checksums, and
  upgrade notes for anything that moves data.
* **An automated test suite** for the ledger and the mesh, running in CI on every commit: double-entry
  invariants, tombstone propagation, and conflict resolution on reconnect.
* **One conference talk and a written version**, delivered at a Perl event or recorded for one, with
  slides and notes published for people who were not in the room.

Success looks like this: a second developer can read the guide, clone the repository, cut a release,
and add an app without asking me anything. That is the test, and it is written down so the Grants
Committee can hold me to it.

## Timetable

Six months, part-time at roughly 0.4 FTE, with a public artefact every month.

* **Month 1** — release process, CI, signing; guide outline; chapters 1–2 drafted. Release 1.
* **Month 2** — ledger test suite (double-entry invariants); chapter 3. Release 2.
* **Month 3** — mesh test suite (tombstones, reconnection conflicts); chapter 4. Release 3.
* **Month 4** — chapters 5–7; test suite green in CI. Release 4.
* **Month 5** — chapters 8–10; an external reader reviews the draft. Release 5.
* **Month 6** — final edit, diagrams, publication; talk delivered and written up. Release 6, the
  guide, and the talk.

The schedule is deliberately sized below the current development rate. The project is presently
developed at a much higher intensity, and the grant should not depend on that continuing.

A monthly progress report will be filed with the Grant Manager, as the Rules of Operation require,
even in a month where no progress was made.

## About the Grantee

I learned Perl at a public library. I had a two-year business diploma and a job at a call centre, and
I had put off going for years because I had lost a copy of *Brave New World*. When I finally went, I
found *Learning Perl*. It looked like something I could actually learn. For the next few months I
worked until after midnight, came home, read and wrote code, slept, and did it again.

Perl is still my preferred language because it lets me design what I am thinking instead of
negotiating with the language first. On Halloween 2022 I started writing code again, and I have been
building JawnOS ever since: more than 138,000 lines of Perl and Mojolicious, Sereal over Unix sockets
between workers, Minion for background jobs, SQLite encrypted at rest, and firmware for three
low-cost boards. I wrote it by hand for three years and eleven months; agentic tooling arrived last
month, largely because I had always assumed someone else would eventually finish it.

This would be my first grant. A sample chapter of the guide is in the repository under
`docs/CHAPTER-02.md`, and the live image is linked from jawnos.ca.

## Grant Amount

The grant is proposed for **USD 6,000.00**. Under the Rules of Operation the grantee will request an
interim payment of up to half the grant amount (USD 3,000.00) during the grant period, subject to the
Grants Committee's approval, with the remainder paid on completion after the final report is
evaluated and published.

* Architecture guide: USD 3,000.00
* Release engineering and CI: USD 1,200.00
* Test suite: USD 1,500.00
* Conference talk and travel: USD 300.00

The request covers roughly a third of the hours involved; the remainder is already committed. There is
no salary line and no equipment line — the grant buys artefacts that outlive it.

## Proposed Grant Manager

The grantee does not propose a Grant Manager and asks the Grants Committee to appoint one. The grantee
is new to the Perl community and has no existing relationship with a committee member. The Rules of
Operation provide that the Committee assigns a manager to each funded grant, and that managers need
not be members of the Committee. An introduction to anyone willing to take the role would be welcome.

