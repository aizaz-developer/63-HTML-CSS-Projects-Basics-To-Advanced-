The <header> Tag
What it is: Introductory content for a page or a section. Typically contains headings, logos, or navigation.
Code snippet:
HTML
<header>
    <h1>My Daily Routine</h1>
    <p>A look into how I spend my day</p>
</header>
When to use it:
At the top of your page for the site title, logo, or intro
Can also be used inside <section> or <article> for section headers
The <main> Tag
What it is: The primary content of the document. There should be only one <main> per page, and it cannot be nested inside <article>, <aside>, <footer>, <header>, or <nav>.
Code snippet:
HTML
<main>
    <!-- All the primary page content goes here -->
</main>
When to use it:
Wrap the central content that is unique to this page
Exclude repeated elements like navigation bars or footers
The <section> Tag
What it is: A thematic grouping of content, typically with a heading. It divides your page into logical chunks.
Code snippet:
HTML
<section>
    <h2>Morning Routine</h2>
    <p>I wake up at 6 AM and drink water...</p>
</section>

<section>
    <h2>Evening Routine</h2>
    <p>After work, I go for a run...</p>
</section>
When to use it:
When you have distinct, themed blocks of content
Each section usually has its own heading (<h2>, <h3>, etc.)
The <footer> Tag
What it is: Footer content for a page or a section. Typically contains author info, copyright, contact links, or related documents.
Code snippet:
HTML
<footer>
    <p>Written by [Your Name]</p>
    <p>Last updated: August 2026</p>
</footer>
When to use it:
At the bottom of your page
Can also be used inside <section> or <article>
Full Semantic Page Structure
HTML
<body>
    <header>
        <h1>Page Title</h1>
    </header>

    <main>
        <section>
            <h2>Section Heading</h2>
            <p>Content...</p>
        </section>

        <section>
            <h2>Another Section</h2>
            <p>More content...</p>
        </section>
    </main>

    <footer>
        <p>Footer content</p>
    </footer>
</body>
