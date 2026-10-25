---
import BaseHead from '../components/BaseHead.astro';
import FormattedDate from '../components/FormattedDate.astro';
import { SITE_TITLE, SITE_DESCRIPTION } from '../consts';
import { getCollection } from 'astro:content';

const posts = (await getCollection('blog')).sort(
    (a, b) => b.data.pubDate.valueOf() - a.data.pubDate.valueOf()
);
---

<!doctype html>
<html lang="en">
    <head>
        <BaseHead title={SITE_TITLE} description={SITE_DESCRIPTION} />
        <style>
            body {
                font-family: 'MyCustomFont', sans-serif;
                margin: 0;
                padding: 0;
                display: flex;
                flex-direction: column;
                min-height: 100vh;
                color: rgb(var(--gray-dark));
                background: rgb(var(--background));
            }
            header {
                display: flex;
                justify-content: space-between;
                align-items: center;
                padding: 1.5rem 2rem;
                background-color: #ace1af;
                color: #1b3b2b;
            }
            header h2 {
                margin: 0;
                font-size: 1.25rem;
            }
            header h2 a {
                text-decoration: none;
                color: #1b3b2b;
            }
            main {
                flex: 1;
                width: 960px;
                max-width: calc(100% - 2rem);
                margin: auto;
                padding: 3rem 0;
            }
            section ul {
                display: flex;
                flex-direction: column;
                gap: 2rem;
                list-style-type: none;
                padding: 0;
                margin: 0;
            }
            section ul li {
                display: flex;
                flex-direction: column;
                gap: 0.25rem;
            }
            section ul li :global(a) {
                text-decoration: none;
                transition: color 0.2s ease;
            }
            section ul li :global(a):hover h4 {
                color: var(--accent);
            }
            .title {
                margin: 0;
                font-size: 1.5rem;
                color: rgb(var(--black));
                line-height: 1.2;
            }
            .date {
                font-size: 0.95rem;
                color: rgb(var(--gray));
            }
            footer {
                padding: 2rem;
                text-align: center;
                background-color: #ace1af;
                color: #1b3b2b;
                font-size: 0.9rem;
            }
            footer p {
                margin: 0.4rem 0;
            }
            footer a {
                color: #1b3b2b;
                text-decoration: underline;
            }
            .social-links {
                display: flex;
                justify-content: center;
                gap: 1.5rem;
                margin-top: 0.5rem;
            }
        </style>
    </head>
    <body>
        <header>
            <h2><a href="/">Projects & Blog</a></h2>
        </header>
        <main>
            <section>
                <ul>
                    {
                        posts.map((post) => (
                            <li>
                                <a href={`/blog/${post.id}/`}>
                                    <h4 class="title">{post.data.title}</h4>
                                </a>
                                <p class="date">
                                    <FormattedDate date={post.data.pubDate} />
                                </p>
                            </li>
                        ))
                    }
                </ul>
            </section>
        </main>
        <footer>
            <p>Contact: <a href="mailto:CollinTCrews@gmail.com">CollinTCrews@gmail.com</a></p>
            <div class="social-links">
                <a href="https://linkedin.com" target="_blank" rel="noopener noreferrer">LinkedIn</a>
                <a href="https://youtube.com" target="_blank" rel="noopener noreferrer">YouTube</a>
            </div>
        </footer>
    </body>
</html>
