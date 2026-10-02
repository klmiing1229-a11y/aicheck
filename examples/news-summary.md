# Example: a news summary before you act on it

This is a real test run from 2 October 2026. The AI had summarised about 40 news headlines on the Anthropic and
OpenAI IPOs. The user was following the story because they hold funds exposed to both companies.

**User:** aicheck

> *(The previous AI reply, shortened:)* Anthropic aims to go public before Thanksgiving (26 Nov 2026), possibly
> mid-November, with investor marketing from the week of 9 November. It seeks a valuation of about US$2 trillion. A
> leaked draft filing shows US$4.6 billion revenue, a US$42 billion net loss and US$84.5 billion committed to SpaceX
> for compute. OpenAI says it has no IPO timeline, is reportedly raising US$30 billion at about US$1.4 trillion, and
> paused AI training twice in three months after agents escaped a test environment.

**aicheck:**

Same model that wrote it, so this flags risks. It does not confirm anything.

**Checking:** a summary of IPO news built from headlines, not the full articles
**Used for:** not stated, assumed following news that affects the user's investments
**Stakes:** medium to high: money could follow, and everything is newer than the model's training data

| # | Claim | Risk | Check it by |
|---|---|---|---|
| 1 | The figures come from a "leaked filing" | 🔴 | Search "Anthropic" on SEC EDGAR (sec.gov/edgar) for an S-1, the form a company files to go public. If none is public, every filing figure below is secondhand |
| 2 | Lists mid-November or before Thanksgiving; marketing from the week of 9 Nov | 🔴 | Find the original Bloomberg story by searching its headline on bloomberg.com. All three timing claims say "reportedly" |
| 3 | US$4.6B revenue, US$42B net loss | 🔴 | First reported by a small site. Compare with a Reuters or Bloomberg report on the same filing, or with EDGAR if #1 finds one |
| 4 | OpenAI paused training twice after agents escaped a test environment | 🔴 | A dramatic claim from one outlet. Look on openai.com/news for a statement and search Reuters for the event. If neither has it, drop it |
| 5 | Valuations of about US$2T (Anthropic) and US$1.4T (OpenAI) | 🟡 | Search each figure plus "Reuters". Headlines often round, or mix up a target with a reported number |
| 6 | OpenAI "has no IPO timeline" | 🟡 | One headline says "no timeline", another says "not this year". Read the CEO's original interview quote |
| 7 | US$84.5B to SpaceX for compute | 🟡 | Single source. Check it the same way as #3 |

+4 lower-risk claims not listed.

**Check first:** #1, because if no filing is public, the revenue, loss and SpaceX figures are rumour and shouldn't drive an investment decision.
**Safe to use as-is:** the overall picture as a summary of what's being reported: Anthropic is likely in November, OpenAI is unlikely in 2026, nothing is confirmed.

Next? (check it for me / fix the answer / done)

**User:** fix the answer

**aicheck:** Nothing is checked yet, so this only marks the risks. Say "check it for me" first for a real fix.

> Anthropic aims to go public before Thanksgiving (26 Nov 2026), possibly mid-November, with investor marketing from
> the week of 9 November. [unverified] It seeks a valuation of about US$2 trillion. A leaked draft filing [unverified]
> shows US$4.6 billion revenue, a US$42 billion net loss [unverified] and US$84.5 billion committed to SpaceX for
> compute. OpenAI says it has no IPO timeline, is reportedly raising US$30 billion at about US$1.4 trillion, and paused
> AI training twice in three months after agents escaped a test environment. [unverified]

*(Only the four 🔴 claims get a tag. Tagging every sentence would show that nothing was checked, but wouldn't tell you where to look.)*
