---
layout: post
title: "🚀 Hacking the AI Overview: How I Used Gemini and Python to Find SEO Blind Spots"
date: 2025-11-26
description: "A few weeks ago, my uncle, who lives in the Seattle area, called me. He’s tired of fighting the relentless moss that thrives on his roof due to the constan"
tags: [GEO, AIO, Technical SEO]
original_source: https://www.linkedin.com/pulse/hacking-ai-overview-how-i-used-gemini-python-find-seo-randy-holland-uzedc
---

### The Scenario: My Uncle, Seattle Rain, and a Search Result That Made No Sense

A few weeks ago, my uncle, who lives in the Seattle area, called me. He’s tired of fighting the relentless moss that thrives on his roof due to the constant PNW rain. He mentioned a high-ranking metal roofing contractor—one of the key accounts at the digital marketing agency I contract for—and he asked, **"Why can't I find them in the quick summaries Google gives me?"**

He was referring to **AI Overviews (AIOs)**.

As the SEO Specialist on the account, I knew this contractor consistently ranked #1 for high-value local queries like **“standing seam metal roof installers Seattle”** and **“best metal roofing for rainy climate Seattle.”** Their transactional pages were dominating the SERPs. Yet, the AI Overviews—the very feature designed to answer informational questions—were consistently citing competitors.

This launched me into a deep dive to understand *exactly* how Google’s Gemini model was processing these high-intent searches.

### 🔑 The Breakthrough: A Peek Under the Hood of AI Search Logic

The core problem wasn't a lack of ranking; it was a lack of **informational coverage** that the AI could easily digest and cite.

The key to solving this lies in a lesser-known feature of the [Gemini API: the grounding metadata](https://ai.google.dev/gemini-api/docs/google-search#:~:text=Grounding%20helps%20you%20build%20applications,sources%20for%20the%20model%27s%20claims.). This metadata reveals the exact "[fan-out queries](https://dejan.ai/blog/hacking-gemini/)" the model generated internally to find its information. Essentially, it shows the AI's internal research logic.

Using a simple Python script in **Google Colab** (and a little help from the Gemini API), I started feeding the model the initial search questions relevant to the agency's client account.

Your company or client might dominate local SERPs. But are they appearing for informational queries in Google's AI Overviews.

**The Insight:** The AI was not just searching the initial prompt; it was *fanning out* to a cluster of **six highly specific, long-tail informational needs** (e.g., durability, material comparisons, and specific material problems like moss).

### 💡 The Missing Link: Why the Client Was Invisible to the AI

The client's existing content was focused on conversion (service pages, CTAs) and was successfully ranking. But it lacked dedicated, extractable, high-authority content that answered the AI's complex research questions.

Of the six "fan-out" queries the AI was using, the agency's content only partially addressed three. **Three massive informational content gaps were discovered**:

1. **"durable metal roofing Seattle"** (Needs a localized, comparative guide).
2. **"metal roofing moss mildew resistance"** (Needs a definitive piece on material science).
3. **"metal roofing types for heavy rain"** (Needs a feature-focused technical breakdown).

### ✅ The Result: Content that Lifts Both Local SEO and LLM Visibility

This technical discovery led to a clear, actionable content strategy that I presented to the agency's content team. We didn't need to reinvent our SEO. We just needed to be cited for the *why* and the *how*.

The agency developed three new, hyper-focused blog posts—one for each missing fan-out query—with structures designed for AI extraction (tables, bulleted lists, immediate answers).

We then internally linked these new, authoritative **informational** pieces to the client's existing, high-ranking **transactional** service pages.

The outcome was nearly immediate: **Within two weeks, the client started being cited in AI Overviews for those high-value informational queries.**

By serving the AI's need for objective, authoritative information, we created a new discovery pathway that directly supports the business’s local rankings and conversions—a huge win for the agency and the client.

### Actionable Takeaway for My Network

You don't need to be a Python expert to replicate this process. **The fastest path to insight is leveraging Gemini itself.**

If you’re struggling to capture AI Overviews for your top keywords:

1. **Start with the AI:** Feed your high-value queries into a tool that uses the Gemini model (or directly access the API).
2. **Ask the AI to Help You Code:** If you want to dive into the API/Python, ask Gemini to generate the initial script and explain the groundingMetadata to you. It's the ultimate coding tutor.
3. **Audit the Fan-Outs:** Find the 3-5 sub-topics the AI is researching, and ensure you have a dedicated, expertly written content piece for each one.

***A Note on the Technology:*** *This fan-out query extraction technique relies on accessing the grounding data exposed by the Gemini API (specifically, models like* ***Gemini 2.5 Flash****). This method remains highly valuable for SEOs who may not have direct API access but wish to understand the AI's search logic. As Google continues to iterate on its models (e.g., with future Gemini updates), the specific queries generated or the method of extraction may evolve. Always treat this data as a directional insight into the current AI search environment.*

***Acknowledging Community Insight:***[*Thanks to Chris Long*](https://www.linkedin.com/feed/update/urn:li:activity:7399427086072946688/) *for highlighting this important technical caveat and for sharing that his team* [Nectiv](https://www.linkedin.com/company/nectiv-digital/) *will be* [*testing the Gemini 3 iteration*](https://www.linkedin.com/posts/chris-long-marketing_feel-the-power-we-extracted-60k-fan-out-activity-7401242641687945216-3MRA?utm_source=share&utm_medium=member_desktop&rcm=ACoAAAMaoQYBoQRx-dGpcbahqAj4TlJz6QE_Y8U) *for further changes.*

**The future of SEO isn't just about ranking on the main page; it's about being the definitive, cited source in the AI's final answer. Go find your agency or client's AI blind spots!**
