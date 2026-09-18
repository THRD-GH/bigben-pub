# Building this site in Google Sites

Google Sites cannot host the files in this repository. It has no import, and its Embed
block runs inside a sandboxed iframe, so the page has to be **rebuilt from Sites' own
blocks**, with the copy pasted in. This sheet has everything needed to do that in about
twenty minutes. Paste-ready copy is at the bottom, English and German kept separate.

## What you give up, and what you gain

**You gain**

- Nothing to patch, nothing to upload, no files to lose. Google runs it.
- One fewer account. It is the landlord's existing Google account, the same one that holds
  the Business Profile.
- Editing is a click on the text and typing. Easier for a non-technical owner than any
  file-based host, if the site ever does need an edit.
- Free.

**You give up**

- **The apex domain.** Google's own help says the URL must include a subdomain such as
  `www`. So the site lives at `www.example.ch`, and `example.ch` has to be a redirect set
  up at the DNS host. Some registrars cannot do that redirect at all.
- **The design.** Sites gives you its six themes and its fonts. The claret and gold
  signwriting look in `index.html` is not reachable. You can get close on colour and get
  the wordmark in a display face, but it will look like a Google Site.
- **The privacy paragraph.** A Google Site is served by Google, loads Google resources and
  sets Google cookies. The line "no cookies, no analytics, nothing from third parties"
  becomes false and must be replaced. Replacement text is below.
- **Control of the markup.** No structured data, no control of heading order, no hreflang
  tags, heavier pages.

Neither is wrong. Sites is the better answer if the priority is that nobody ever has to
touch a file again. The files in this repository are the better answer if the priority is
the apex domain, the look, and a page that embeds nothing from anyone.

## Build order

1. **sites.google.com → Blank site.** Name it "Big Ben Pub".
2. **Theme.** Themes → pick *Impression* or *Vision*, then set the colour to a custom dark
   shade. `#1B1013` for the background and `#D8B356` for the accent are the closest match
   to the design in this repository.
3. **Pages.** Rename the home page to `English`. Add a second page named `Deutsch`. The
   two are siblings in the top navigation, which is the language switch.
4. **Header.** Choose the *Title only* header type. Put `BIG BEN` as the title. Sites will
   not letterspace it; leave it.
5. **Sections, in this order, on each page.** Use a *Text box* for each heading and body
   block, and *Button* blocks for the actions:
   - Address line, phone button, Directions button, Instagram button.
   - Open/closed embed. Insert → Embed → Embed code, paste `status-embed.html` from this
     folder, and set `LANG` to `en` or `de` at the top of the pasted code. Drag the box to
     full width and about 60px tall.
   - Live sport. Heading, paragraph, and two buttons to Google and Instagram.
   - Opening hours. Use a two-column table, not a text box, so the times line up.
   - Bar and kitchen. Two columns.
   - The pub. One image and one paragraph. Upload the new photograph here.
   - Finding us. Sites' own Map block is fine here and adds nothing new to disclose,
     because the page is already Google's.
   - Impressum and privacy. A text box at the foot of both pages.
6. **Publish.** Settings → set the web address. Then Custom domain if the domain is ready.

## Custom domain

Google's help: the URL must include a subdomain, so use `www`. Ownership is verified
through Google Search Console with a TXT record, then a `CNAME` for `www` pointing at
`ghs.googlehosted.com`. Allow up to 48 hours. Set the apex `example.ch` to redirect to
`www.example.ch` at the DNS host, or visitors typing the bare domain get nothing.

## Privacy text that is true on Google Sites

Replace the privacy paragraph. The Impressum block is unchanged.

> **Deutsch.** Diese Website wird von Google Sites betrieben und auf Servern von Google
> gehostet. Beim Aufruf einer Seite werden technische Verbindungsdaten, darunter Ihre
> IP-Adresse, an Google übermittelt und dort verarbeitet. Google kann dabei Cookies setzen.
> Einzelheiten finden Sie in der Datenschutzerklärung von Google. Wir selbst erheben keine
> weiteren Daten und setzen keine Analyse-Werkzeuge ein. Wenn Sie uns anrufen oder
> schreiben, verwenden wir Ihre Angaben nur, um Ihre Anfrage zu beantworten.

> **English.** This site runs on Google Sites and is hosted on Google's servers. When you
> open a page, technical connection data including your IP address is sent to Google and
> processed there, and Google may set cookies. See Google's privacy policy for detail. We
> collect nothing further ourselves and use no analytics. If you telephone or write to us,
> we use what you tell us only to answer you.

## Paste-ready copy

### English page

**Header line**
Alte Landstrasse 20 · 8942 Oberrieden ZH

**Buttons**
043 388 55 08 · Directions · Instagram

**Live sport**
We show all the major football and rugby. If there is a match you want to see, ring us and
we will tell you whether it is on.

This week's matches go up on our Google page and on Instagram, usually the day before.

**Opening hours**

| Monday | Closed |
| Tuesday – Wednesday | 17:00 – 22:30 |
| Thursday | 17:00 – 23:00 |
| Friday – Saturday | 17:00 – 23:30 |
| Sunday | 12:00 – 19:30 |

We stay open later for live sport and for events, sometimes a good deal later. The hours
for any particular day are always right on our Google page.

**On the bar**
Guinness, poured properly · Swiss craft beer · Wine by the glass · Single malts

**Bar snacks**
Chicken wings · Fries · Nachos · Toasties · Pies
Snacks only, no full kitchen.

**The pub**
A proper British pub in a village of five thousand people, two minutes from the station.
People meet here halfway between Zurich and Zug, watch the match, and stay for a whisky.

Live Irish music now and then. The whole pub can be hired for private parties. Ring Paul
on 043 388 55 08.

**Finding us**
Alte Landstrasse 20, 8942 Oberrieden ZH
Oberrieden Dorf station, two minutes on foot
About 15 minutes by S-Bahn from Zurich and from Zug
043 388 55 08

No booking system. For a table on a busy match night, or to hire the pub, ring us. We
answer the phone.

### Deutsche Seite

**Kopfzeile**
Alte Landstrasse 20 · 8942 Oberrieden ZH

**Schaltflächen**
043 388 55 08 · Anfahrt · Instagram

**Livesport**
Wir zeigen alle grossen Fussball- und Rugbyspiele. Rufen Sie uns an, wenn Sie ein
bestimmtes Spiel sehen möchten.

Die Spiele der Woche stehen auf unserer Google-Seite und auf Instagram, meist schon am
Vortag.

**Öffnungszeiten**

| Montag | Geschlossen |
| Dienstag – Mittwoch | 17:00 – 22:30 |
| Donnerstag | 17:00 – 23:00 |
| Freitag – Samstag | 17:00 – 23:30 |
| Sonntag | 12:00 – 19:30 |

Bei Livesport und Anlässen bleiben wir länger offen, manchmal deutlich länger. Die Zeiten
für einen bestimmten Tag stehen immer auf unserer Google-Seite.

**An der Bar**
Guinness, richtig gezapft · Schweizer Craft Beer · Wein im Glas · Single Malts

**Kleine Karte**
Chicken Wings · Pommes · Nachos · Toasties · Pies
Nur kleine Gerichte, keine warme Küche.

**Der Pub**
Ein richtiger britischer Pub in einem Dorf mit fünftausend Einwohnern, zwei Minuten vom
Bahnhof. Man trifft sich hier auf halbem Weg zwischen Zürich und Zug, schaut das Spiel und
bleibt auf einen Whisky.

Gelegentlich Irish Live-Musik. Der ganze Pub kann für private Anlässe gemietet werden.
Rufen Sie Paul an unter 043 388 55 08.

**So finden Sie uns**
Alte Landstrasse 20, 8942 Oberrieden ZH
Bahnhof Oberrieden Dorf, 2 Minuten zu Fuss
Rund 15 Minuten mit der S-Bahn von Zürich und von Zug
043 388 55 08

Keine Online-Reservation. Für einen Tisch an einem Spielabend oder für eine private Feier
rufen Sie uns bitte an. Wir gehen ans Telefon.

### Impressum, both pages

[Firma bzw. Name des Betreibers]
Big Ben Pub
Alte Landstrasse 20
8942 Oberrieden, Schweiz

Telefon: 043 388 55 08
E-Mail: [kontakt@domain.ch]
[UID CHE-xxx.xxx.xxx, falls im Handelsregister eingetragen]

Verantwortlich für den Inhalt: [Name]

## Still unverified

Whether a Google Sites editor exists as a phone app could not be confirmed from a reliable
source. It matters little here, because in this plan the landlord never edits the website
at all. Match nights go on the Business Profile. But confirm it before promising anyone
that the site is editable from a phone.
