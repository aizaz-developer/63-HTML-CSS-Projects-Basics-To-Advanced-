# Project 06 Notes: Blog-Style Content & Semantic Text

---

## 1. The `<article>` Tag

**What it is:** A self-contained piece of content that makes sense on its own. It could be ripped out of the page and still be understandable — a blog post, a news story, a product review, or a deep-dive tech article.

**Code snippet:**
```html
<article>
    <h1>Brain-Computer Interfaces: The Future of Human Augmentation</h1>
    <p>Neuralink and other BCI startups are pushing the boundaries...</p>
</article>
When to use it:

When to use it:
Blog posts or tech articles
News stories
Product reviews
Any content that stands alone as a complete piece
Why it matters:
Screen readers can identify the start and end of an independent article
Search engines understand this is the primary content piece
You can have multiple <article> tags on one page (unlike <main>)
2. Heading Levels <h1> Through <h6>
What they are: Six levels of headings that create a document outline. <h1> is the most important, <h6> is the least.
Code snippet:
HTML
<h1>Brain-Computer Interfaces: A Deep Dive</h1>     <!-- Article title -->
<h2>What Is a BCI?</h2>                            <!-- Major section -->
<h3>Invasive vs Non-Invasive</h3>                  <!-- Sub-section -->
<h4>Neuralink's N1 Implant</h4>                    <!-- Sub-sub-section -->
Heading hierarchy rules:
Table
Level	Use Case
<h1>	One per page — the main title
<h2>	Major sections of the article
<h3>	Sub-sections inside <h2>
<h4>–<h6>	Deeper nesting when needed
When to use them:
Never skip levels (don't jump from <h2> to <h4>)
Always use them in order for accessibility
Think of them like a book: <h1> = book title, <h2> = chapters, <h3> = sub-chapters
3. The <blockquote> Tag
What it is: Indicates that the enclosed text is an extended quotation from another source. Browsers typically indent it by default.
Code snippet:
HTML
<blockquote>
    "We are already cyborgs. Your phone and your computer are extensions of you."
</blockquote>
When to use it:
Long quotes that stand alone as a block (multiple lines)
Pull quotes in articles
Testimonials or cited passages
<blockquote> vs <q>:
<blockquote> = block-level, for long quotes, indented
<q> = inline, for short quotes within a paragraph, adds automatic quotation marks
4. The <cite> Tag
What it is: Marks the title of a creative work (book, movie, song, research paper) or the name of the author/source being cited.
Code snippet:
HTML
<p>As <cite>Elon Musk</cite> stated in a recent keynote, BCI technology will redefine human capability.</p>

<!-- Or for the work itself -->
<p>A foundational paper, <cite>Toward Brain-Computer Interfacing</cite>, shaped the field.</p>
When to use it:
Citing a research paper title, book title, or article name
Naming the author, researcher, or speaker of a quoted statement
Can be used inside or outside <blockquote>
5. The <time> Tag
What it is: Represents a specific date, time, or duration in a machine-readable format. Helps search engines and browsers understand temporal information.
Code snippet:
HTML
<!-- Date only -->
<time datetime="2024-01-29">January 29, 2024</time>

<!-- Date and time -->
<time datetime="2026-08-13T09:00">August 13, 2026 at 9:00 AM</time>

<!-- Duration -->
<time datetime="PT8M">8 minutes</time>
The datetime attribute format:
Table
What You Mean	datetime Value
Date	2026-08-13
Date + Time	2026-08-13T14:30
Time only	14:30:00
Duration	PT2H30M (Period Time 2 Hours 30 Minutes)
When to use it:
Publication dates on blog posts
Release dates for tech products or research papers
Event start/end times
Anywhere a date or time appears on your page
6. Putting It All Together
Code snippet:
HTML
<article>
    <header>
        <h1>Brain-Computer Interfaces: Merging Mind and Machine</h1>
        <p>Published on <time datetime="2026-08-13">August 13, 2026</time></p>
    </header>

    <section>
        <h2>What Is a BCI?</h2>
        <p>A brain-computer interface is a direct communication pathway...</p>
    </section>

    <section>
        <h2>Industry Voices</h2>
        <blockquote>
            "The long-term aspiration with Neuralink is to achieve a symbiosis with artificial intelligence."
            <br>
            — <cite>Elon Musk</cite>
        </blockquote>
    </section>

    <section>
        <h2>The Road Ahead</h2>
        <p>As research accelerates, ethical frameworks must evolve alongside the technology...</p>
    </section>

    <footer>
        <p>Written by <cite>Aizaz</cite> | <time datetime="2026-08-13">August 13, 2026</time></p>
    </footer>
</article>
Key Takeaways
<article> wraps self-contained content like blog posts or tech articles
Headings <h1>–<h6> create a document outline — never skip levels
<blockquote> is for long, standalone quotations
<cite> names the creator, author, or title of a creative/research work
<time datetime="..."> makes dates machine-readable for SEO and accessibility
Combine semantic tags to create professional, accessible blog-style content
